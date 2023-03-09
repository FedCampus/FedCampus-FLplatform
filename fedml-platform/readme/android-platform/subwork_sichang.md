# Subwork\_Sichang

TODO: find Android Developer Tutorials for Java.

<details>
<summary>Useless resources since we are not going to use Kotlin.</summary>

## Recommended Android Developer Tutorials

- [x] [Build your first app](https://developer.android.com/training/basics/firstapp)
- [ ] [Training courses](https://developer.android.com/courses)
    - [x] [Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course)
    - [x] [Android Basics in Kotlin](https://developer.android.com/courses/android-basics-kotlin/course)
    - [ ] [Jetpack Compose for Android developers](https://developer.android.com/courses/jetpack-compose/course)
    - [ ] [Modern Android app architecture](https://developer.android.com/courses/pathways/android-architecture)
    - [ ] [Kotlin coroutines](https://developer.android.com/courses/pathways/android-coroutines)
- [ ] [Connectivity](https://developer.android.com/guide/topics/connectivity)
- [ ] [Testing](https://developer.android.com/training/testing)
- [ ] [Security best practices](https://developer.android.com/topic/security/best-practices)

</details>

## Up till 2023/03/05

- Read FedML background materials.
- Ran FedML demo Python simulation.
- Tried Android Studio, Kotlin, JetPack Compose.
- Sketched tech stack plan for the Android platform.

<details>
<summary>Java + FedML Java API, Django + FedML Python API + PostgreSQL, HTTPS poll</summary>

Jiaqi asked me for a formal tech stack plan for the Android platform, here is my current sketch:

Android client app: Single Java app shipped to the user.

- Data gathering: UI, user data collection and handling, and HTTPS client in Java.
- ML: Call FedML's Java API for local training.

Server: Single modular Python server with single database.

- Python as language of choice to best support ML exploration.
- ML module:
    - Call FedML's Python API from the server for aggregation.
- Web module: gather and store data.
    - Django for HTTPS server and database interface (ORM).
    - PostgreSQL for database.

HTTPS does not support broadcasting, and we cannot assume that the clients would always be on. So, I assume that the clients will poll the server for new information ever so often. We only need to implement a REST API or something equivalent for the communication.

```mermaid
graph TD;
    K(Java Android app)-->|directly call|J(FedML Java API);
    K-->|poll|S(Django Server)
    S-->|respond|K
    S-->|communicate|D(PostgreSQL)
    S-->|use API|M(Python ML module)
    M-->|call|P(FedML Python API)
```

</details>

- Looked for full-duplex communication protocol as demanded by Jiaqi.

<details>
<summary>Need an external push service.</summary>

For [Push API][Push API], I only found [instruction to make push messages][make-push-message] which is for web apps. Unofficial instructions to make push messages to Android exist on [Intercom Developers][intercom-push-notifications] and [Iterable][iterable-push-notifications], both of which use Firebase for the push service.

My *conclusion* is that we should consider these after we have a working poll model because they involve external services.

</details>

## Up till now

TODO: find Android HTTPS client in Java instead.

<details>
<summary>Useless since we are not going to use Kotlin.</summary>

- Looked for Android HTTPS client resources.
    - [Perform network operations
        overview][perform-network-operations-overview] from Android developers.
    - [Ktor][ktor] the Kotlin HTTPS client/server library.
    - [android/connectivity-samples][android-connectivity-samples],
        a Git repository of code samples.

    But, I figured out that I should first learn how to separate code in
    modules in Android apps.

</details>

- Checked out the previous Android app `FedC`.
    - The app architecture is similar in Java, although the UI uses XML.
    - `org.eclipse.paho.client.mqttv3` handles MQTT.
    - The connection blocks the main thread, causing UI lag.

[Push API]: https://developer.mozilla.org/docs/Web/API/Push_API
[make-push-message]: https://developers.google.com/learn/pathways/pwa-push-notifications
[intercom-push-notifications]: https://developers.intercom.com/installing-intercom/docs/react-native-push-notifications
[iterable-push-notifications]: https://support.iterable.com/hc/en-us/articles/115000331943-Setting-up-Android-Push-Notifications-#_1-set-up-firebase-for-your-android-app
[perform-network-operations-overview]: https://developer.android.com/training/basics/network-ops
[ktor]: https://ktor.io
[android-connectivity-samples]: https://github.com/android/connectivity-samples

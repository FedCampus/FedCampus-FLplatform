# June Evaluation

July 5

## Goal attainment

The goal of the last month was to build a platform for on-device federated
learning (FL) training using Flower and support pipelined machine learning (ML)
model deployment.

I have developed a working FL training platform,
but am still waiting for Johnny on deployment.
I have designed and implemented the ML model deployment infrastructure,
but the back-end-based ML model swapping has not been tested, yet,
for the lack of ML models to test.

I built the FL training platform [`dyn_flower_android_drf`][dyn_flower_android_drf]
upon the Flower Android Example.
I wrapped Flower server with Django REST Framework (DRF) to control the
which ML model to use and collect telemetry on demand.
As suggested by Beilong, I also revamped the `.tflite` file generation process
and the on-device training using the latest TensorFlow Lite (TFLite) APIs.

Despite the complexity from Android Development and using TFLite, currently,
the most difficult challenge is to understand the use case of the platform.
The HealthKit demo only collects 3 numbers per day per user,
and "the algorithm team" has not proposed any use case for the data.

Facing the obstacles, I worked on additional sidetracks for efficiency.
I added Federated Analytics (FA) to `FedCampus_APP`.
And, I investigated simulation for building a benchmark platform.

One bonus is the interest from the Flower community in our project.
A few people have reached out to me to discuss on Flower and Android.
It is also highly possible that our work can be upstreamed to Flower to
contribute to their Android SDK platform.

## Skills development

Besides the Android development experience and DRF, I mainly learned about
TFLite operation logic and APIs.
Other skills include:

- Various Kotlin language constructs.
    - Suspend functions.
    - Generic functions with `reified` type parameters.
    - Functional-program-style language constructs such as `Sequence<T>`.
- FA by differential privacy (DP).
    - Laplace Mechanism in the FA for `FedCampus_APP`.
- Python annotations.
    Simplified the `.tflite` file generation script in
    `dyn_flower_android_drf/gen_tflite`.

Arguably, some of the above skills were time-consuming to learn,
and I could have worked around them.
But, I feel like we avoided some technical debt,
and the knowledge would benefit us in the future.

## Collaboration and teamwork

As a team member, I mentored others as well as discussed about directions.
I mentored Aicha on the structure of our training platform.
I mentored Beilong on on-device training and general programming practices.
I also discussed with Beilong on various task like HealthKit data obtainment
and discussed with Johnny on deployment strategies.

The greatest challenge in collaboration was not the lack of knowledge,
it was people who were confident that they got it while they probably didn't.
But, like how Beilong finally move to write real Git commit messages instead
of "update," maybe it just takes repetitive explanation and some time.

Despite working closely with my teammates, I can tell some of them are afraid
of me.
People indicated that they were afraid of me looking down upon them for skill
issues,
which means that I need to work on my geniality.
Moreover, the team severely lacks hype and motivation.
I am still working on letting them think that they work for their individual
goals.

## Reflection and growth

As we block on teamwork, I think the next step would be to further decouple the
work to work on separate, fully responsible parts.
A clear, practical goal also seems to be missing for the team.
Besides helping the team, I also need to clarify my personal goal.

My current goal would be to upstream my work to Flower Android SDK,
make our platform support iOS, and develop a benchmark platform.

[dyn_flower_android_drf]: https://github.com/FedCampus/dyn_flower_android_drf

# This is a Gradle support plugin for Qase application

## Exposed tasks

### `qaseTest`
  - Either (1) delegates execution to the `java` plugin of Gradle or (2) runs a test-plan scoped subset of `@CaseId`-annotated methods.
  - Requires the `java` plugin of Gradle to be present during the build.
  - If `QASE_RUN_ID` variable is not specified and `QASE_TEST_PLAN_ID` is present among the environment variables, a test-plan scoped run is triggered.
  - Additional environmental variables and test framework options are still required to be specified additionally.

## Proof-of-Concept (POC) projects

For your convenience, I created 2 POC projects:

- [Junit/TestNG](https://github.com/mbirintsev/qase-java/qase-gradle-plugin-poc-junit)
- [Cucumber](https://github.com/mbirintsev/qase-java/qase-gradle-plugin-poc-cucumber)

To test the plugin, kindly, utilize the command below:

* Linux: `./gradlew qaseTest -DQASE_API_TOKEN=your_token -DQASE_TEST_PLAN_ID=your_plan_id -DQASE_PROJECT_CODE=your_project_code -DQASE_URL="https//api.qase.io/v1"`
* Windows: to be tested

If you need test values for `-DQASE_*` variables, feel free to edit the code of the POC tests for your test-plan on Qase platform. However, you can reach me out and ask for test values. 

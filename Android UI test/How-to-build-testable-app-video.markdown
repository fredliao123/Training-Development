## The [video](https://www.youtube.com/watch?v=VJi2vmaQe6w&t=198s)

## Keypoints
- Speed <--> Scope <---> Fidablity
- Unit test -> Integration test -> E2E test
- Group app by layers, data layer, business layer and presentation layer. Changing logic in lower layer like data layer can lead to a large rewrite in the app. Also, this leads to a large E2E test codebase and takes lots of time to run. 
- How to decompose the app affects largely the ability to write good test suite. Decompose by feature instead of layers is better(What we are doing is correct). This way integration test can be focused on each feature. And unit test can be focused on the logic in this feature, such as `AccountRepo`. 
- Start the coding process by writing tests first. From top down, E2E test first, then integration test and down to unit tests.

### E2E test: 
Run on a real or vitual android device. Blackbox testing. 
```
fun createTask() {
	ActivityScenario.launch(TasksActivity::class.java)
	onView(WithId(R.id.fab_add_task)).perform(clicl())
	// ...
}
```

### Integration tests:
Tests all the units collaborate as planned. The difference between E2E test and integration test is that E2E test can be across screens testing user flow. But integration test should focus on one screen.
Because integration tests is more foucsed on collaboration

This reproduces an issue where method signatures in the detekt baseline appear differently 
depending on whether the method has a doc comment.

To reproduce the problem:
1. Run `./gradlew detekt` and observe that it passes
2. Edit `Example.kt` to remove the method-level doc comment
3. Run detekt again and observe that if fails
4. Run `./gradlew detektBaseline` and observe that the `baseline.xml` changes

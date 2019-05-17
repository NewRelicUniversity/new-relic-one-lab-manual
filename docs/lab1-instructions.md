Lab 1: Using the Tags API
=========================

Objective
---------
Use the Tags API to add a tag to a New Relic Browser application.

Instructions
------------
1. Visit the New Relic GraphQL API Explorer: [https://api.newrelic.com/graphiql](https://api.newrelic.com/graphiql).
2. Select the training account’s API key from the dropdown list near the top of the window.
3. In the left-hand pane, write an _entitySearch_ query to find the `guid` of the Browser application named “New Relic Pet Clinic”. _Hint (select text to reveal):_ <span>You are looking for an entity whose <em>name</em> is 'New Relic Pet Clinic' in the <em>domain</em> of 'BROWSER'.</span>
4. Click the _Execute query_ button near the top of the window to execute your query. See the result in the right-hand pane.
5. If you get an error or do not see a `guid` in the result, return to Step 3 and try again. Otherwise, proceed to Step 6.
6. Write a _taggingAddTagsToEntity_ mutation, passing the `guid` returned above, and adding a `tag` with a key of “training” and a value of your name. _Hint:_ <span>Tag values are an array, so you must surround them with square brackets.</span>
7. Execute your mutation, ensuring that no errors are returned in the result.
8. _Optional:_ Write and execute an _entity_ query to view the tags associated with the New Relic Pet Clinic Browser application.
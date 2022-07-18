# mtb-schema

These are the schema for the m2c2 assessments in the mtb app. These schema describe the data that is created when a participant completes trials.

Data are returned from the m2c2 assessments through a callback function that returns an `ActivityDataEvent` object. The two relevant properties on this object are:

* `newData`
* `data`

`newData` is the data that was created by the just-completed trial. `Data` is all the data that have been created since the participant started the assessment. 

If you plan to persist the data as soon as a trial is completed, you should use the `newData` property and save each trial when you receive it. `newData` is described by the Json Schema in `single-trial`.

 Alternatively, if you want to save only when all trials are complete, you should use the `data` property. `data` is described by the Json Schema in `all-trials`

You will use the schema from only one of these folders, depending on your persistence strategy.

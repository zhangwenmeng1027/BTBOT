# BTBOT


The BTBOT code and executable files have already been uploaded to the Docker Hub website. You only need to retrieve the Docker image using the following command:

```bash
docker pull btbot123/btbot
```

Below, we demonstrate the execution results of BTBOT by solving a sample task.

For example, you can solve the demo task (automatic charging task, consistent with the one in the paper) by running the following commands:

```bash
cd /BTBOT
./dist/main_pre_check_change --task "demo" --url "https://* * *" --key "* * *" --llm "gpt-4o"
```

- The `url` field should contain the LLM API endpoint, for instance, the OpenAI API URL when using ChatGPT.
- The `key` field should include your API key.
- The `llm` field specifies the model to use, such as `gpt-4o`, `gpt-3.5-turbo`, `gpt-4-turbo`, or other models.

The `task` field represents the name of the task to solve. To solve other tasks, you only need to modify the `task` field value. For example, use `"charge"`, `"demo"`, `"doTask"`, or `"get_food"`. A complete list of tasks is recorded in the `benchmark.xlsx` file.

To view BTBOT's performance on 70 benchmark tasks, execute the following command. The output will display the task name and the corresponding BT for each task:

```bash
./dist/script --result "result" --url "https://* * *" --key "* * *" --llm "gpt-4o"
```

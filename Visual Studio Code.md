# Error & Solution
## Error 1
```
Error loading webview: Error: Could not register service workers: InvalidStateError: Failed to register a ServiceWorker: The document is in an invalid state..
```
## Solution
Solved following [this answer](https://stackoverflow.com/a/69316961/8775499). To kill other vscode process(es) in Ubunbtu, execute the below command,
```
killall code
```


##### launch.json
```
"args": ["--pro_train=1", "--save_model=1",  "--save_dir=/home/zayed/Research/Modulated GCN/Modulated_GCN/Modulated-GCN_benchmark/ckpt/debug_mode/", "--root_path=/home/zayed/Research/Modulated GCN/Modulated_GCN/Modulated-GCN_benchmark/dataset/", "--post_refine", "--save_out_type=post", "--sym_penalty=1", "--co_diff=1", "--show_protocol2"]
```


Python > Terminal: Activate Environment

---

### Reference
1. [How to Debug PyTorch Source Code - Deep Learning in Python](https://youtu.be/el39D7rz7K0)
2. [Python debugging in VS Code](https://code.visualstudio.com/docs/python/debugging)
3. [Visual Studio Code: How debug Python script with arguments](https://stackoverflow.com/questions/51244223/visual-studio-code-how-debug-python-script-with-arguments)

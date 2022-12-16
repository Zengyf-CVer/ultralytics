## Installation
!!! note "Latest Stable Release"
    ```
    pip install ultralytics
    ```
??? tip "Development and Contributing"
    ```
    git clone https://github.com/ultralytics/ultralytics
    cd ultralytics
    pip install -e '.[dev]'
    ```
    See contributing section to know more about contributing to the project


## CLI
The command line YOLO interface let's you simply train, validate or infer models on various tasks and versions.
CLI requires no customization or code. You can simply run all tasks from the terminal
!!! tip
    === "Syntax"
        ```bash
        yolo task=detect    mode=train  model=s.yaml    epochs=1 ...
                   ...             ...          ...
                 segment          infer       s-cls.pt
                 classify         val         s-seg.pt
        ```

    === "Example"
        ```bash
        yolo task=detect mode=val model=s.yaml 
        ```
        TODO:  add terminal screen/gif
[CLI Guide](#){ .md-button .md-button--primary}

## Python API
Ultralytics YOLO comes with pythonic Model and Trainer interface. 
!!! tip
    ```python
    import ultralytics
    from ultralytics import YOLO

    model = YOLO()
    model.new("s-seg.yaml") # automatically detects task type
    model.load("s-seg.pt") # load checkpoint
    model.train(data="coco128-segments", epochs=1, lr0=0.01, ...)
    ```
[API Guide](#){ .md-button .md-button--primary}
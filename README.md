# ds6050-group1-project

# Data

# Caltech
https://data.caltech.edu/records/f6rph-90m20

## Download Data
```bash
wget "https://data.caltech.edu/records/f6rph-90m20/files/data_and_labels.zip?download=1" -O caltechpedestriandataset.zip
```

## Convert to YOLO label format
```bash
python caltech-preprocessing-yolo.py
```

```yaml
path: /datasets/caltechpedestriandataset
train: /images/train
val: /images/val
    
nc: 1
    
names: [
    'person'
]
```

## Convert to COCO label format

**Train**
```bash
python yolo-to-coco.py --path_to_annotations /home/ybt7qf/ds6050-group1-project/datasets/calt
echpedestriandataset/labels/train/ --path_to_images /home/ybt7qf/ds6050-group1-project/datasets/caltechpedest
riandataset/images/train/ --name caltechpedestriandataset_train
```

**Val**
```bash
python yolo-to-coco.py --path_to_annotations /home/ybt7qf/ds6050-group1-project/datasets/calt
echpedestriandataset/labels/val/ --path_to_images /home/ybt7qf/ds6050-group1-project/datasets/caltechpedest
riandataset/images/val/ --name caltechpedestriandataset_val
```
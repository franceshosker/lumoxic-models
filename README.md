# Lumoxic Models

Pre-optimized model zoo from [Lumoxic AI](https://lumoxicai.me). Ready-to-deploy compressed models.

## Available Models

### Image Classification

| Model | Size | Accuracy | Target |
|-------|------|----------|--------|
| ResNet-50 INT8 | 12.1 MB | 93.8% Top-1 | Server |
| MobileNetV3 INT8 | 5.4 MB | 74.8% Top-1 | Mobile |
| EfficientNet-B0 INT8 | 5.1 MB | 76.7% Top-1 | Edge |

### NLP

| Model | Size | Accuracy | Target |
|-------|------|----------|--------|
| BERT-Base INT8 | 68 MB | 88.4% F1 | Server |
| DistilBERT INT8 | 42 MB | 85.9% F1 | Server |

### Object Detection

| Model | Size | Accuracy | Target |
|-------|------|----------|--------|
| YOLOv8-M INT8 | 8.4 MB | 88.6% mAP50 | Server |

## Usage

```python
import onnxruntime as ort
session = ort.InferenceSession("resnet50-int8.onnx")
result = session.run(None, {"input": image_data})
```

## Custom Optimization

Use the [Lumoxic API](https://lumoxicai.me/playground) to optimize your own models.

(c) 2026 Lumoxic AI.
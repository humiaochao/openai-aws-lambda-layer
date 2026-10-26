# OpenAI AWS Lambda Layer

Pre-built AWS Lambda Layer containing the `openai` Python SDK 3.37.0 for Python 3.14 ([Download](./openai-aws-lambda-layer-py314.zip)).

Note: This layer was built and tested on x86_64.

## How to Use

To add and configure the layer to AWS Lambda functions, follow the official AWS guidelines: [AWS Documentation on Managing Lambda Event Function dependencies with layers](https://docs.aws.amazon.com/lambda/latest/dg/invocation-layers.html).

## How It Was Built

You can build this layer yourself by following the steps below:

```bash
python3.14 -m venv venv
source venv/bin/activate
mkdir python
cd python
pip3 install openai==3.37.0 -t .
cd ..
zip -r openai-aws-lambda-layer-py314.zip python
deactivate
```

Note: if you want to the latest `openai` Python SDK version instead of 3.37.0, use `pip3 install openai -t .` instead of `pip3 install openai==3.37.0 -t .`.


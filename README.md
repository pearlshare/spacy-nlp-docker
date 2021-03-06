# spacy-nlp

SpaCy python3

- Installs English tagger, parser and NER
- Installs English GloVe vectors

## Getting started

- Build locally

```
docker build -t spacy-nlp:en .
```

- (OR) Get latest from hub.docker.com

```
docker pull pasupulaphani/spacy-nlp:en
```

## Run tests

```
sh test.sh
```

### Get shell

```
docker run -it spacy-nlp /bin/bash
```

-------------------------------------

# spacy-nlp-zeromq

SpaCy with zeromq bindings

## Getting started

- Build locally

```
docker build -f Dockerfile.zeromq -t spacy-nlp-zeromq:en .
```
- (OR) Get latest from hub.docker.com

```
docker pull pasupulaphani/spacy-nlp-zeromq:en
```


### Get shell

```
docker run -v ${PWD}:/usr/zeromq --publish 4242:4242 --entrypoint=/bin/bash  -it spacy-nlp-zeromq:en
python3 /usr/zeromq/zeromq/server.py
```


# Troubleshoot

Check if port is open

```
if ! nc -z 0.0.0.0 4242 2>&1 >/dev/null; then echo "NOT AVAILABLE"; fi
```

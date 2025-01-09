# Dockerfile Bug: Missing requirements or incorrect script path
This repository demonstrates a common error when building Dockerfiles. The issue lies in either the missing `requirements.txt` file or an incorrect path to the application script in the `CMD` instruction.

## Bug Description:
The provided `Dockerfile` attempts to install dependencies using `pip3` but fails due to a missing or incorrectly specified `requirements.txt` file. The `CMD` instruction could also have an incorrect path. 

## Solution:
The solution involves ensuring that `requirements.txt` is present in the same directory as the `Dockerfile` and correcting the path of the script in the `CMD` instruction if needed. 

## How to Reproduce the Bug:
1. Clone this repository.
2. Attempt to build the Docker image using `docker build -t my-app .`.
3. Observe the build failure.

## How to Fix the Bug:
1. Ensure `requirements.txt` exists and contains the correct package dependencies. 
2. Verify that `app.py` (or the correct script name) is located in the root directory of the Docker image context.
3. Rebuild the image.
# Expo Camera Video Corruption Bug

This repository demonstrates a bug in the Expo Camera API related to video recording corruption. The issue occurs when switching cameras (front/rear) while a video recording is in progress.  The recorded video file becomes corrupted and unplayable.

## Bug Description

The bug manifests when using the Expo Camera API to record videos and switching the camera type during recording.  While the recording appears to continue seamlessly, the resulting video file is not playable, indicating data corruption. The Expo Camera API doesn't provide feedback or an error to signal this issue.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run the app using `expo start`.
4. Start a video recording.
5. Switch between the front and rear cameras while recording.
6. Stop the recording.
7. Attempt to play the recorded video - it will likely be unplayable.

## Solution

A complete solution requires a fix within the Expo Camera API itself.  However, a workaround is to pause the recording before switching cameras and resume recording afterward to avoid data corruption.
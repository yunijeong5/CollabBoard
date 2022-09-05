# CollabBoard

## Overview

CollabBoard is a simple collaborative whiteboard that can be accessed from multiple web browsers. Any drawings made on one user's window are immediately refelcted on others. Locally, a user can change their brush color or clear the window.

<img src='https://i.imgur.com/YLbQWc3.gif' title='Video Demo' width='' alt='Video Demo' />

## Dependencies

- Flask: a Python micro web framework.
- Faker: A library for generating fake data.
- twilio: A library for communicating with the Twilio API.
- python-dotenv: A library for importing environment variables from .env file.

## How it works

Twilio Sync's Message Streams syncronize multiple browser windows at a high rate and low latency.

## Future

- Launch the web app to sync multiple users on difference devices.
- Change stroke size or shape.
- Create url specific to a group's use, enabling multiple user groups to collaborate on their own whiteboards.

## Bugs

- Resizing the browser after drawing on it alters or clears the drawing.

## Installation

**Requirements**: _Python 3.6+, a free Twilio account to use their API._

1. Clone the repo and build the environment:

```
$ git clone https://github.com/yunijeong5/CollabBoard.git
$ cd CollabBoard
$ python3 -m venv venv  # use "python -m venv venv" on Windows
$ . venv/bin/activate  # use "venv\Scripts\activate" on Windows
(venv) $ pip install -r requirements.txt

```

Remane the `.env_sample` file to `.env` and fill the variables in it (you'll need a free [Twilio account](http://www.twilio.com/referral/w6qBg0)).

Run the application with

```
(venv) $ flask run
```

Finally, open [http://localhost:5000/](http://localhost:5000/) on multiple tabs to see the sync in action!

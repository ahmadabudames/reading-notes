# API Deployment

**This article is intended for engineers who use the Django framework. It gives a deep insight into configuring Django project settings, and the pros and cons of different approaches. In the article, you will also find recommendations concerning tools, best practices and architectural solutions, all time-tested and proven by successful projects.**


## Managing Django Settings: Issues

- **Different environments**. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings (for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django setting configurations.

- **Sensitive data**. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.

- **Sharing settings between team members**. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.

- **Django settings are a Python code**. This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.


## Setting Configuration: Different Approaches

***There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of recommendations and approaches on how to do it best. Let’s take a brief look at the most popular ones to examine their weaknesses and strengths.***


> Pros:
- Secrets not in VCS.

> Cons:
- settings_local.py is not in VCS, so you can lose some of your Django environment settings.

- The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.

- You need to have settings_local.example (in VCS) to share the default configurations for developers.

## Separate settings file for each environment

**This is an extension of the previous approach. It allows you to keep all configurations in VCS and to share default settings between developers.**

## 12 Factors

**12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider.**


> **As the name suggests, the collection consists of twelve parts**:

- Codebase

- Dependencies

- Config

- Backing services

- Build, release, run

- Processes

- Port binding

- Concurrency

- Disposability

- Dev/prod parity

- Logs

- Admin processes



## What is SSH

SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.


## Understanding Different Encryption Techniques


**The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host. There are three different encryption technologies used by SSH:**

- 1-Symmetrical encryption

- 2-Asymmetrical encryption

- 3-Hashing.






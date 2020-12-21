# Augpier

- We asked insight_worker to send data to "http://bears.sociallycompute.io:5105/storeZapier"
- When "http://bears.sociallycompute.io:5105/storeZapier" receives data, it stores them in a list. We created an empty list in server.py. 
- We also created an API for Zapier to get data, which is "http://bears.sociallycompute.io:5105/zapier". When Zapier send request to this route, it dumps the data of the aforementioned list.
- After Zapier receives data, it triggers actions of another app, such as sending an email to users' gmail. 

## Examples of integrating Augur into Zapier.
### Create Authentication

- Create Authentication
![Authentication1](docs/Augier_screenshots/1auth.png)

- Include an API url (Zapier can get data from this API)
![Authentication2](docs/Augier_screenshots/2auth.png)

- Test it
![Authentication3](docs/Augier_screenshots/3auth.png)

### Create an Augur Trigger

- Name the trigger
![trigger4](docs/Augier_screenshots/4trigger.png)

- Include an API url
![trigger5](docs/Augier_screenshots/5trigger.png)

- Test it
![trigger6](docs/Augier_screenshots/6trigger.png)

- Define output
![trigger7](docs/Augier_screenshots/7trigger.png)

### Zap the Augur with other apps

- Choose a trigger
![zap8](docs/Augier_screenshots/8zap.png)

- Choose an action
![zap9](docs/Augier_screenshots/9zap.png)

- Let's try Gmail
![zap10](docs/Augier_screenshots/10zap.png)

- Choose a Gmail account, and send a mail from Gmail to another email address
![zap11](docs/Augier_screenshots/11zap.png)

- Choose Augur data to send
![zap12](docs/Augier_screenshots/12zap.png)

- Test it
![zap13](docs/Augier_screenshots/13zap.png)

- Check email inbox. Received!
![zap14](docs/Augier_screenshots/14zap.png)

- Another example. Zap it to Google Doc
![zap15](docs/Augier_screenshots/15zap.png)

- Append Augur data to an existing Google Doc file
![zap16](docs/Augier_screenshots/16zap.png)

- Test it
![zap17](docs/Augier_screenshots/17zap.png)

- Succeed!
![zap18](docs/Augier_screenshots/18zap.png)

Once you integrate Augur into Zapier, you can zap it with different apps. 



# Augur

branch | status
   --- | ---
master | [![Build Status](https://travis-ci.com/chaoss/augur.svg?branch=master)](https://travis-ci.com/chaoss/augur)
   dev | [![Build Status](https://travis-ci.com/chaoss/augur.svg?branch=dev)](https://travis-ci.com/chaoss/augur)


[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2788/badge)](https://bestpractices.coreinfrastructure.org/projects/2788)

## What is Augur?

Augur is a software suite for collecting and measuring structured data
about [free](https://www.fsf.org/about/) and [open source](https://opensource.org/docs/osd) software (FOSS) communities.

We gather trace data for a group of repositories, normalize
it into our data model, and provide a variety of metrics about said
data. The structure of our data model enables us to synthesize data
across various platforms to provide meaningful context for meaningful
questions about the way these communities evolve.

We are a [CHAOSS](https://chaoss.community>) project, and many of our
metrics are implementations of the metrics defined by our awesome community. You
can find more information about [how to get involved on the CHAOSS website](https://chaoss.community/participate/).

## Collecting Data

One of Augur's core tenets is a desire to openly gather data that people can trust, and then provide useful and well-defined metrics that help give important context to the larger stories being told by that data. We do this in a variety of ways, one of which is doing all our own data collection in house. We currently collect data from a few main sources:

1. Raw Git commit logs (commits, contributors)
2. GitHub's API (issues, pull requests, contributors, releases, repository metadata)
3. The Linux Foundation's [Core Infrastructure Initiative](https://www.coreinfrastructure.org/) API (repository metadata)
4. [Succinct Code Counter](https://github.com/boyter/scc), a blazingly fast Sloc, Cloc, and Code tool that also performs COCOMO calculations

This data is collected by dedicated data collection workers controlled by Augur, each of which is responsible for some querying some subset of these data sources. We are also hard at work building workers for new data sources. If you have an idea for a new one, [please tell us](https://github.com/chaoss/augur/issues/new?template=feature_request.md) - we'd love your input!


## Getting Started

If you're interested in collecting data with our tool, the Augur team has worked hard to develop a detailed guide to get started with our project which can be found [in our documentation](https://oss-augur.readthedocs.io/en/master/getting-started/toc.html).

If you're looking to contribute to Augur's code, you can find installation instructions, development guides, architecture references (coming soon), best practices and more in our [developer documentation](https://oss-augur.readthedocs.io/en/master/development-guide/toc.html). Please know that while it's still rather sparse right now,
but we are actively adding to it all the time. If you get stuck, please feel free to [ask for help](https://github.com/chaoss/augur/issues/new)!

## Contributing

To contribute to Augur, please follow the guidelines found in our [CONTRIBUTING.md](CONTRIBUTING.md) and our [Code of Conduct](CODE_OF_CONDUCT.md). Augur is a welcoming community that is open to all, regardless if you're working on your 1000th contribution to open source or your 1st. We strongly believe that much of what makes open source so great is the incredible communitites it brings together, so we invite you to join ours!

## License, Copyright, and Funding

Copyright © 2020 University of Nebraska at Omaha, University of Missouri and CHAOSS Project at the Linux Foundation

Augur is free software: you can redistribute it and/or modify it under the terms of the MIT License as published by the Open Source Initiative. See the [LICENSE](LICENSE) file for more details.

This work has been funded through the Alfred P. Sloan Foundation, Mozilla, The Reynolds Journalism Institute, and 9 Google Summer of Code Students.

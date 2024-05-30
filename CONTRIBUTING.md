# Contributing to Bellingcat Tools

Hello! Thanks for being part of the Bellingcat Tech Community :muscle: We really appreciate your ideas, thoughts, and involvement. Read on for guidance on how to contribute to our projects :trophy:

Contributions to Bellingcat projects are released to the public under the project's open source license.

Please note that this project is released with a [Contributor Code of Conduct](./CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

We welcome contributions of all sizes, from typo fixes to complete refactors. However, for larger contributions or significant changes to our projects, please reach out to our team by opening an issue or by emailing [contact-tech@bellingcat.com](mailto:contact-tech@bellingcat.com); we'll be able to provide early-stage feedback and give advice on how to structure your changes for the best chance of your PR(s) being accepted.

## Considerations for Tool Development :thinking:

### What programming language should be used?

The wider open source research community generally uses Python as a programming language for tools. We encourage developers to use Python for tools because of its ubiquity, support, and relative ease of use. We are also most familiar with Python, so it helps us support and maintain tools if they are written in Python.

Of course there are some scenarios where using Python isn’t the most suitable language, or isn’t what developers were familiar with, and that’s absolutely fine - we value the community benefit of tools regardless of programming language. For example, the [Uniform Timezone tool](https://github.com/bellingcat/uniform-timezone) is a Chrome extension written in JavaScript.

### How developed should a tool be?

We like to think of our tools as sitting on a ladder that balances accessibility and effort:

0. Editable Python script
0. Library API
0. Command Line Interface
0. Jupyter Notebook/Google Colab
0. Full User Interface

**An editable script** is where many tools start life, and these sit at the least accessible and lowest effort end of the ladder. To use tools at this stage of development, a user must have Python installed on their machine, some technical expertise and confidence to configure the script correctly. A script is a great prototype for a tool, but will probably only find a narrow technical audience.

**The Library API** is an incremental improvement in accessibility, meaning the tool may reach a slightly broader technical audience, and still requires coding confidence from a user. Importantly, a library API enables us to distribute a tool via the Python Package Index and lays a firm foundation for subsequent development.

**A Command Line Interface (CLI)** provides a significant step up in terms of accessibility, but still requires a user to have Python installed on their machine. [Research by Bellingcat](https://www.bellingcat.com/resources/2022/08/12/these-are-the-tools-open-source-researchers-say-they-need/) suggests that a significant part of the online researcher community is unable to use the command line. CLI tools don’t require any coding experience to use, but do require technical confidence with the command line. 

**[A Jupyter Notebook](https://jupyter.org/)** can be an effective way to create a simple front-end for Python (and some CLI) tools. Using a notebook as an interface to a Library API makes it much easier for a non-technical user to access a tool, particularly if the notebook is used through a service like [Google Colab](https://colab.research.google.com/) (or self-hosted with [Binder](https://mybinder.org/)). There are ways to create simple user interfaces for notebooks to make using them even more accessible.

**A Graphical User Interface (GUI)** is one of the best ways to make a tool accessible to the most people, but it can require a lot of extra development work. Before building a user interface, consider if a notebook would be a more suitable implementation. We tend to prefer web apps over desktop apps as we think they are generally more accessible. We don’t strongly advocate a particular front-end framework, but think that [Streamlit](https://streamlit.io/) is pretty good - it’s a pure Python way to quickly build a web app.

### Does Bellingcat host all tools?

No, though we will try to deploy each tool on a suitable platform. When deciding whether to host a tool, we consider the benefits to the open source research community as well as cost, liability, and maintainability.

Tools that are hosted are much more widely used than other tools (such as CLIs and Desktop Apps), so we try to get tools hosted where possible (by Bellingcat or otherwise).

Even if we can’t host a tool, we will try to make the code available on GitHub.

### Do tools need unit tests?
No, we don’t require testing as part of our tools. This decision is to reduce the knowledge required to make a technical contribution. Formal testing is welcomed, but is not needed. We are most interested in tests that cover the most likely failure modes of a tool (such as a third-party API changing etc).

## Submitting a pull request :bulb:

0. Fork and clone the repository
0. Create a new branch: `git checkout -b some-descriptive-name`
0. Make your changes, using clear commit messages
0. Push to your fork and submit a pull request
0. Sit back, relax and wait patiently for your pull request to be reviewed and merged.

Here are a few things you can do that will increase the likelihood of your pull request being accepted:

- Follow standards for style and code quality.
- Keep your change as focused as possible. If there are multiple changes you would like to make that are not dependent upon each other, consider submitting them as separate pull requests.
- Use clear and concise commit messages (i.e. `fix date format parsing bug`).

## External Resources :link:

- [How to Contribute to Open Source](https://opensource.guide/how-to-contribute/)
- [Using Pull Requests](https://help.github.com/articles/about-pull-requests/)

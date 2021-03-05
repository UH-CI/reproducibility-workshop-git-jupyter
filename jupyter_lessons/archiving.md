# Archival of Research Products
Adapted from https://reproducible-science-curriculum.github.io/publication-RR-Jupyter

In this lesson we will learn about why appropriate online archival of digital research inputs and outputs is an important part of promoting reproducibility. Specifically, research inputs such as data, source code, and notebooks that become digitally unavailable or inaccessible due to insufficient archiving for perpetuity are a major impediment to reproducibility.

## Learning objectives

- Define and describe the importance of archiving research inputs and outputs.
- Select appropriate archival services for different types of research objects.
- Define benefits of acquiring globally unique resolvable identifiers for digital resarch objects archived online.

## Online archiving of digital research inputs and products

### Why archives for research inputs and products, and why use them

A not so uncommon story:  _You’re a graduate student reading a paper on which you want to base your analysis approach, and for you therefore need to verify and reproduce the analysis. The paper gives the lab's website as the link for obtaining the code. However, it turns out the researcher has since left that university, and their new lab's website no longer has a link to that code. You contact the author directly to ask about the code that the paper claims to be available from the lab website. After several weeks of silence the author responds that they will try and find the code, but they're working on a different project now. That was a month ago._

**Lab websites aren't archives.** Doing online archiving well is non-trivial, and likely isn't your line of research. Use an online archive that specializes in doing well what you need from an archive.

Journal supplemental materials are popular for digital archiving (they are typically free for the author) but often suffer from a number deficiencies when compared to a bona-fide online archive:
* Impoverished or lack of independent indexing for findability
* Paywalled if the article is paywalled
* Lack of direct download link
* Only manuscript-oriented formats supported (PDF, MS Word)
* No separate citation and unique identifier

There are _many_ archives, for all imaginable purposes and domains.  In fact, there are so many that there is [re3data](http://www.re3data.org), a registry of currently >2000 repositories that allows browsing them by various attributes.

> ## Exercise 1
>
> * Identify requirements and desirable features for an archive for a non-manuscript research product of your choice. Compare to lab website archiving and journal supplemental materials.
{: .challenge}

> ## Exercise 2
>
> Identify the research products that underly and support a manuscript of yours in preparation (or one recently published if those research products became supplementary materials or were not published). Consider the following choices of repositories for fit for purpose:
>
> * [Dryad](http://datadryad.org)
> * [Zenodo](http://zenodo.org)
> * [Harvard Dataverse](https://dataverse.harvard.edu)
> * [Figshare](http://figshare.com)
> * [Journal of Open Source Software](http://joss.theoj.org)
> * Your university's Institutional Repository (IR)
> * A public source code repository ([Github](http://github.com), [Bitbucket](http://bitbucket.com), [Gitlab](http://gitlab.com) etc)
>
> Explain your preferences, and compare to lab website and supplemental material archiving.
{: .challenge}

## Stable, globally unique, and resolvable identifiers for research products

### Why globally unique resolvable identifiers for non-paper research products?

One of the key benefits of using an archive is that nearly all of them will assign a globally unique resolvable identifier to deposits. Deposit identifiers benefit both depositors, and those reusing deposits, i.e., all of an archive's primary users:
* Identify and cite the deposit in a manuscript and a CV
* Track views, downloads, or more generally impact
* Identify exactly what record, and which version of it was (re)used

### Why DOIs

DOIs (digital object identifiers) are only one type of unique identifier, but is the most frequently used type in scholarly communication, and for identifying research products. Some of its benefits include:

* Allows separating content from who hosts the content.
* Cannot be minted ad-hoc, and instead requires interacting with a registration agency, which typically need to be paid a fee. This fosters metadata quality, and assigns clear responsibility for maintaining the DOI's continued resolution.
* Publishers, and the publishing industry, knows how to deal with them.
* Practically every scholar knows how to deal with them.

> ## CrossRef versus DataCite
>
> While DOIs on the surface all look the same, some expectations for their associated metadata (and [programmable APIs](http://citation.crosscite.org/docs.html) differ based on the issuing DOI registrar (often referred to as "type of DOI"). In scholarly publishing and communication, the most frequently encountered DOI registrars are [CrossRef](https://www.crossref.org) (issues almost all scientific paper DOIs, works with publishers) and [DataCite](https://datacite.org). The latter is used for all kinds of "other" research products, including data, software, source code, and preprints.
{: .discussion}



# Publishing

# Authoring & Citation

In addition to LICENSE, it is recommended to add:

- **AUTHORS**: file containing the list of contributors
- **CITATION**: file containing information on how to cite your work, including a DOI (Digital Object Identifier)

## List of authors

A GitHub repository is very often created by an individual user so adding the list of authors is very important.

> ## Add a new file AUTHORS in your repository
>
> - Go to your repository in your web browser
> - Click on "Create new file" and name your file `AUTHORS`
> - Add the list of authors/contributors and commit your changes
>
{: .challenge}

## Make your GitHub repository citable (<a href="https://en.wikipedia.org/wiki/Digital_object_identifier#">DOI</a>)

Your GitHub repository contains your scientific workflow, your programs/software, datasets (or links to your datasets) and jupyter dashboards so it is important to make the work you share on GitHub citable by archiving your GitHub repository to get a DOI. You may have a Data archive in your University or you may use the data archiving tool <a href="https://zenodo.org/">Zenodo</a>.

### Login to Zenodo

- Go to <a href="https://zenodo.org/">https://zenodo.org/</a> and click on `Log in` (not `Sign up`)
- Choose `Log in with GitHub`

<img src="../../images/zenodo_login.png" width="30%">


- Zenodo will redirect you back to GitHub and ask you to give Zenodo the permissions it needs. click `Authorize Application`:

<img src="https://guides.github.com/activities/citable-code/zenodo-authorize.png" width="50%">

**Source**: <a href="https://guides.github.com/activities/citable-code/zenodo-authorize.png">https://guides.github.com/activities/citable-code/zenodo-authorize.png</a>

### Get a DOI for your Github repository

- When sucessfully login to Zenodo, click on your username (top right) and select `GitHub`

<img src="../../images/zenodo_github.png" width="70%">

Then
- Select the repository `sharing-github` and flip the switch to `on`
- Create a <a href="https://help.github.com/articles/creating-releases/">Release on Github</a>
- Then go to your GitHub repository and click on `settings` and select `Webhooks`

<img src="../../images/webhooks_github.png" width="70%">

Your GitHub repository is now linked to Zenodo and you will automatically get a DOI:


<img src="../../images/zenodo_archive_github.png" width="70%">

### Add your DOI to your GitHub repository

- Get your DOI badge on Zenodo and copy your DOI information (selection markdown)

<img src="../../images/zenodo_DOI_github.png" width="50%">

- Go to your GitHub repository and edit your README file to add your DOI
- Create a new file CITATION in your GitHub repository and show how to cite your reprository with your DOI

# Limitations

Sharing your GitHub repository along with your jupyter notebooks/dashboards is an important step for making your research reproducible. However, anyone willing to rerun your programs/dashboards/notebooks need to get the same computational environment (python, additional python packages, etc.).

The next section (using <a href="https://github.com/jupyterhub/binderhub">Binder</a>) will show you how to make your research fully reproducible, offering users the same computational environment with no efforts.

> ## Where to find more about GitHub
> To learn more about GitHub you can review one or more of these additional (external) resources:
> - GitHub Guide - [Hello World](https://guides.github.com/activities/hello-world/)
> - All the [GitHub guides](https://guides.github.com)
> - Hubspot [`git` and GitHub tutorial](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)
> - Plurlsight's [GitHub beginner's guide](https://www.pluralsight.com/blog/software-development/github-tutorial)
> - Code School's [GitHub tutorial](https://www.codeschool.com/courses/mastering-github)
{: .discussion}

> ## More about Git version control
> If you would like to learn about source code version control using the `git` software, the `git` in GitHub, please see these resources:
> - Try this 15 minute interactive  [`git` tutorial](https://try.github.io/)
> - Try some additional `git` exercises [here](https://gitexercises.fracz.com)
{: .discussion}

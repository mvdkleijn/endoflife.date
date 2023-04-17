---
title: Ceph
category: os
iconSlug: ceph
permalink: /ceph
versionCommand: ceph versions
releasePolicyLink: https://docs.ceph.com/en/latest/releases/
changelogTemplate: "https://docs.ceph.com/en/__LATEST__/releases/__CODENAME__/"

auto:
  - git: https://github.com/ceph/ceph.git
    regex: ^v(?<major>0|[1-9]\d*)_(?<minor>0|[1-9]\d*)_(?<patch>\d{1,3})_?(?<tiny>\d+)?$
    template: '{{major}}.{{minor}}.{{patch}}{%if tiny %}p{{tiny}}{%endif%}'

identifiers:
  - repology: ceph

# A list of releases, supported or not (mandatory).
# Releases must be sort from the newest (on top of the list) to the lowest.
# Do not add releases that are not considered "stable" (such as RC/Alpha/Beta/Nightly).
releases:

-   releaseCycle: "17"
    codename: quincy
    releaseDate: 2022-04-19
    support: true
    eol: 2024-06-01
    extendedSupport: false
    latest: "17.2.6"

    # Latest release date (optional).
    # Use valid dates, and do not add quotes around dates.
    latestReleaseDate: 2022-01-23

    # Whether this is a "LTS" release (optional, default = false).
    # What LTS means may differ from product to product (see LTSLabel above).
    # Only provide for a release that will get much longer support than usual.
    lts: true

    # Whether this is a "discontinued" release (optional).
    # Can be set to true/false.
    # Only use if discontinuedColumn is set to true.
    discontinued: true

    # A link to the changelog for the latest release
    # (optional, default = the URL generated from changelogTemplate if it is provided).
    # Use this if the link is not predictable (i.e. you can't use changelogTemplate),
    # or if the changelogTemplate generated link must be overridden.
    # Do not use a localized URL (such as one containing en-us) if possible.
    # Use the special value 'null' (unquoted) if you want to disable link for a specific cycle of a
    # product having a changelogTemplate.
    link: https://example.com/news/2021-12-25/release-1.2.3

# In the following markdown section, ensure that all the above are present:
# 1. A one line statement about what the product is, with a link to the primary website (in a quote).
# 2. A short summary of the release policy, pointing out the EoL policy as well, if available.
# 3. Any additional information that may be of interest.
#
# See also the Guiding Principles on the wiki ( https://github.com/endoflife-date/endoflife.date/wiki/Guiding-Principles )
# for indication on the tone and voice to use for the text.


# Please leave a newline both above and below the triple-dashes.

---

# All the product information text should be under triple-dashes.
# If you are adding any images in the text, they might get blocked due to our CSP.
# So prefer using releaseImage in such cases. Note that images on the same website as releaseImage
# will not be blocked.

> [Time Turner](https://jkrowling.com/time-turner) is a device that powers short-term time travel.

Time-turners are no longer released, and the last known stable release was in HP.5 release.

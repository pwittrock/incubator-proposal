# Proposal for Incubator Project: Reference Docs (*reference-docs*)

## Problem Statement

The existing Kubernetes reference documentation has gotten us very far,
but is due for a makeover.  Elements that can be improved include:
styling / look and feel, structural organzation around object and
operation relationships, inclusion of example config and code, and
improved names / titles.

As an example of ways we can improve upon our current solutoin,
 the [Stripe Api Documentation](https://stripe.com/docs/api)
 has been held up as an example of easy to use reference documentation.
[Slate](https://github.com/lord/slate) is an example of a doc framework
that provides similar structure.

## Proposed Solution

Build our own tooling to produce a set of reference documents for the
Kubernetes API and tools inspired by what we consider best-in-class
api reference docs.  A proof of concept has been build upon the
[brodocs](https://github.com/Birdrock/brodocs) framework for the
[api operations](http://docs.k8s.replicatingperfection.net/),
[resource types](http://resources.k8s.replicatingperfection.net/), and
[kubectl client](http://kubectldocs.k8s.replicatingperfection.net/).

The proof of concept was generated from the open-api-spec.json produced
by kubernetes + a configuration file for information not present
in the open-api-spec.json.  The example code was all manually added
in the form of yaml files.

## Roadmap

- [ ] Q4 2016 Code dump of proof of concept
- [ ] Q1 2017 Code refactor and cleanup
- [ ] Q1 2017 Proof of concept promoted to blessed Api documentation on k8s.io
- [ ] Q2 2017 Open api extensions added to remove need for config file
- [ ] Q2 2017 Support for apis served by federated api severs
- [ ] Q3 2017 Graduation to Kubernetes project


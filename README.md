# CloudFormation test — custom repository tag key

A single SNS topic tagged with a non-default repository key (`CodeKeeperRepo` instead of
`RepositoryId`), to check repository resolution uses the tag key configured on the
repository, not a hardcoded default. The repository is registered with that same key, so
an edit addressed by the topic ARN resolves and completes; a resolver that only read the
default key would fail to find the repository.

Target: `AlertsTopic` DisplayName (root template `codekeeper-test-cfn-ctag.yaml`).

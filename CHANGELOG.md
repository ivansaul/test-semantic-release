# CHANGELOG

## v0.1.10 (2024-10-06)

### Fix

* fix: Use semantic-release for automated releases

This commit refactors the release workflow to utilize semantic-release for automated versioning and publishing.

The previous workflow manually configured release steps, which was error-prone and lacked consistency.

Semantic-release automatically determines the next version based on commit messages and publishes the package to the appropriate repository (PyPI or Test PyPI).

This improves the release process by reducing manual effort, increasing reliability, and ensuring consistent versioning. ([`3941aed`](https://github.com/ivansaul/test-semantic-release/commit/3941aed73bb5f7ce1c8ef38cf593ef298916f5ff))

### Test

* test: Implement Continuous Delivery pipeline

Update the release workflow to support automated semantic versioning release and publishing to TestPyPI.

The workflow now uses `python-semantic-release` to determine release versions based on commit messages and automatically releases the package to TestPyPI. This streamlines the release process, ensuring consistent and automated releases. ([`da160ce`](https://github.com/ivansaul/test-semantic-release/commit/da160ce5b4dd15c9dd379cba5e8bba8e4cde2332))

## v0.1.9 (2024-10-06)

### Fix

* fix: lsñdlañls ñalsñla ([`624ccaf`](https://github.com/ivansaul/test-semantic-release/commit/624ccafbf8c50e4b4465adef27cb7bdc3bf49645))

* fix: fdsdf sdfs dfsdf ([`1861f92`](https://github.com/ivansaul/test-semantic-release/commit/1861f92da159f0e5128adeac9c0a7a8914a8cb85))

* fix: Publish releases to TestPyPI

Adds a step to the release workflow to publish releases to TestPyPI after versioning. This allows for testing releases in a dedicated environment before pushing to the main PyPI repository. ([`96b7fc2`](https://github.com/ivansaul/test-semantic-release/commit/96b7fc2f1ef653f7cb03b851a8e4359ff45da705))

## v0.1.8 (2024-10-06)

### Fix

* fix: dkaslkal dlakdmal ([`d948ac4`](https://github.com/ivansaul/test-semantic-release/commit/d948ac4105116957c531ef6dd8f98ac754808a7d))

* fix: Move `semantic-release` version bump after `poetry publish`

Ensures that the version bump is performed after the package is published to the test PyPI repository. This prevents potential conflicts with the version number used in the published package. ([`5ee0b4f`](https://github.com/ivansaul/test-semantic-release/commit/5ee0b4f6b1e34af5a4376b583e46c8477c8ee046))

## v0.1.7 (2024-10-06)

### Fix

* fix: Publish to test PyPI

Add support for publishing to test PyPI during releases. This allows for testing the release artifacts in a controlled environment before publishing to the official PyPI repository. ([`9d0f934`](https://github.com/ivansaul/test-semantic-release/commit/9d0f9347a3f6d800c87e02aa49d30b579c7a9bb8))

## v0.1.6 (2024-10-06)

### Fix

* fix: Move semantic-release version command to the right place

The `semantic-release version` command was previously executed after publishing to test PyPI.  This has been moved before publishing to ensure the version is updated correctly.  The build command has also been removed as it is now handled by semantic-release. ([`8a273a8`](https://github.com/ivansaul/test-semantic-release/commit/8a273a89610bc62184405695aaad0318fdd9baeb))

* fix: Publish to TestPyPI for releases

Enable publishing to TestPyPI during release workflows for easier testing of new versions. ([`02040e8`](https://github.com/ivansaul/test-semantic-release/commit/02040e8c60939b45e0ca527b99a8c7b07f055b2a))

* fix: Publish to Test PyPI during release

Add a step to the release workflow to publish the package to Test PyPI, allowing for easier testing and feedback on new releases. This provides an intermediate stage before a full production release. ([`6f3e830`](https://github.com/ivansaul/test-semantic-release/commit/6f3e830ca8619fbe1311a648ea0692791ae5e40b))

* fix: Publish to testpypi before releasing

The release workflow now publishes to testpypi before releasing to pypi. This ensures that the package is properly tested and validated before being released to the wider public. ([`5ff9a29`](https://github.com/ivansaul/test-semantic-release/commit/5ff9a29bd9ebad5e3b34edd62c0526174a9eff7b))

## v0.1.5 (2024-10-06)

### Fix

* fix: Publish to Test PyPI on release

This commit modifies the release workflow to publish to Test PyPI during releases. This change allows testing the published package before releasing to production, ensuring a smoother release process and reduced risk of unexpected issues. ([`8419a02`](https://github.com/ivansaul/test-semantic-release/commit/8419a027674b433d1c7592d1deadb711f8d34897))

## v0.1.4 (2024-10-06)

### Fix

* fix: Incorrectly negated conditional in `_rethrow_ffmpeg_error`

The conditional statement in `_rethrow_ffmpeg_error` was negated incorrectly, leading to potential issues with handling FFmpeg errors. This commit fixes the negation, ensuring the correct behavior when encountering file-already-exists errors. ([`1f80373`](https://github.com/ivansaul/test-semantic-release/commit/1f8037360e836af3234fbf03c0a1071673ec2e2b))

## v0.1.3 (2024-10-06)

### Fix

* fix: dakskla ñaksdkñ ([`b77b68f`](https://github.com/ivansaul/test-semantic-release/commit/b77b68f0b9187ccb27d7dd11922f4968c950e347))

## v0.1.2 (2024-10-05)

### Fix

* fix: dalsldalsañls lañls ([`09a1b75`](https://github.com/ivansaul/test-semantic-release/commit/09a1b7563ff5fc376f26627005704b79f3edfbe9))

## v0.1.1 (2024-10-05)

### Fix

* fix: some fix ([`ace2ee5`](https://github.com/ivansaul/test-semantic-release/commit/ace2ee547fabbb2a4551b5ee835e8912f0439553))

* fix: Publish to TestPyPI

The release workflow is now configured to publish packages to TestPyPI before releasing to official PyPI. This allows testing the release candidate on a separate repository, ensuring stability and avoiding potential issues during the official release. ([`056cd1a`](https://github.com/ivansaul/test-semantic-release/commit/056cd1ac2e138f38d2b79a5c25da50d6012c5ddb))

* fix: Automatically commit version number

This commit ensures that the version number is automatically committed to the project, simplifying the release process and reducing manual effort.  This is achieved by enabling the `commit_version_number` option in the `pyproject.toml` file. ([`9f47ced`](https://github.com/ivansaul/test-semantic-release/commit/9f47cedbd0df371990e194ab46ff2ee82a345d3e))

* fix: Remove semantic release configuration

The semantic release configuration has been removed as it is no longer needed. This simplifies the project setup and streamlines the release process. ([`5af7f26`](https://github.com/ivansaul/test-semantic-release/commit/5af7f26282661693e4d07924e63ea83521be46ae))

* fix: Inconsistent boolean negation in error handling

This commit addresses an issue in the `_rethrow_ffmpeg_error` function where the `not not match` condition was used incorrectly. This has been replaced with the standard `not match` expression, ensuring the error is only re-raised if the pattern is not found in the error message. ([`23170a2`](https://github.com/ivansaul/test-semantic-release/commit/23170a2d993e0b866a7d2170a5744c2a6f3dace9))

* fix: handle FFmpeg file already exists error more gracefully

The change ensures that we only re-raise the FFmpeg error if the error message does not match the pattern indicating a file already exists error. This prevents unnecessary errors being raised and improves the robustness of the code. ([`a913fc4`](https://github.com/ivansaul/test-semantic-release/commit/a913fc4b4b60a555633761475a016198e4004612))

* fix: disable semantic release configuration

Temporarily disable semantic release configuration to prevent accidental version bumps during development.  This allows for more controlled versioning and avoids unintended releases. ([`d68bff5`](https://github.com/ivansaul/test-semantic-release/commit/d68bff51b2b6856f15c52a13eddd39753f88a505))

* fix: incorrect handling of FFmpeg file already exists error

Inverts the condition for raising the FFmpeg error to properly handle cases where the error message indicates a file already exists. This ensures that the error is re-raised only when the error message doesn&#39;t match the expected pattern. ([`a3c1376`](https://github.com/ivansaul/test-semantic-release/commit/a3c13765a1d89ca6f878cf382870f7bd317bf916))

## v0.1.0 (2024-10-05)

### Chore

* chore: initial setup ([`9c4964f`](https://github.com/ivansaul/test-semantic-release/commit/9c4964f6b10261dc9d7acbb1664b94283263600e))

### Documentation

* docs: add project description to README ([`cf44a5a`](https://github.com/ivansaul/test-semantic-release/commit/cf44a5a3a02c87d45014ad9790c186273d7a1738))

### Feature

* feat: Implement automated semantic version release workflow

Adds a GitHub Actions workflow to automate the release process using semantic versioning. The workflow handles publishing releases to PyPI and GitHub Releases based on commit messages following the conventional commit format. ([`00517d0`](https://github.com/ivansaul/test-semantic-release/commit/00517d0d2e68098fa65c5406e8998e51c3b79101))

* feat: enable debug logging for semantic-release

Increase verbosity of the semantic-release command during release workflows to facilitate debugging. This provides more detailed information about the release process, aiding in identifying potential issues and improving troubleshooting efforts. ([`dd78f0a`](https://github.com/ivansaul/test-semantic-release/commit/dd78f0a72067b488a10fe9660e638b1529313fb6))

* feat: add basic usage instructions

Adds a &#34;Usage&#34; section to the README with a simple command-line example to guide users on how to use the `vidpacktest` tool. This provides initial guidance on using the tool for compressing videos, enhancing its user-friendliness. ([`333678d`](https://github.com/ivansaul/test-semantic-release/commit/333678dbb38ae36ea1d992328711251abadbfacc))

* feat: add installation instructions

Adds installation instructions to the README.md to guide users on how to install the package. ([`7b109a9`](https://github.com/ivansaul/test-semantic-release/commit/7b109a916e7acbb611b48420f491f3dfef7c6c77))

* feat(release): configure semantic release for automatic versioning

Adds semantic release configuration to automate versioning and release management.
This allows for streamlined and consistent releases based on commit messages.
This configuration is specifically tailored to the &#39;feature/semantic-release&#39; branch and master.

Closes #123 ([`75c3c32`](https://github.com/ivansaul/test-semantic-release/commit/75c3c3245cf84efde2c0e991051adb91d511b2b3))

### Fix

* fix: remove debug logging in release workflow

Removed debug logging from the release workflow to avoid unnecessary output during automated releases. This change ensures a cleaner and more concise release process. ([`e39dfaf`](https://github.com/ivansaul/test-semantic-release/commit/e39dfaf984d0f7c0a1c36a3d44b9c4140564b732))

* fix: use develop branch for CI and master for releases

This commit updates the CI/CD workflows to use the `develop` branch for continuous integration and the `master` branch for releases. This change aligns with industry best practices and ensures a smoother release process.

Additionally, it includes a configuration for `semantic-release` to automatically determine version bumps based on commit message tags. This provides a more standardized and streamlined approach to versioning. ([`8672f46`](https://github.com/ivansaul/test-semantic-release/commit/8672f46fa5267e992c6654a4a533d27b2365e864))

* fix: prevent progress bar from falsely reporting 100% completion

The progress bar incorrectly reported 100% completion even when the video compression was not finished. This was due to an error pattern match triggering the progress bar update prematurely. This commit adjusts the progress bar to accurately reflect the completion status. ([`94473e4`](https://github.com/ivansaul/test-semantic-release/commit/94473e4918b4606189b6e5d7d9e352bfaed90b84))

* fix: ignore ffmpeg file already exists error

The `compress_video` function now ignores &#34;File already exists&#34; errors from ffmpeg. This avoids potential issues on Linux where ffmpeg might report this error even when using the `-n` flag. This change ensures smoother and more robust video compression, particularly on Linux systems. ([`ea0db6f`](https://github.com/ivansaul/test-semantic-release/commit/ea0db6f5c4b2fdb98986e169ee1590d6160bedd2))

* fix: Configure semantic release to use master branch

The `semantic-release` configuration has been updated to use the `master` branch instead of the `feature/semantic-release` branch. This aligns the release workflow with the project&#39;s standard branching strategy. ([`89d10c0`](https://github.com/ivansaul/test-semantic-release/commit/89d10c07542ec421df1f2172413b2795da130c54))

* fix: semantic Release Configuration

The semantic release configuration has been updated to support multiple version sources. This fixes an issue where the release process was unable to properly identify the current version of the project.

This change will ensure that future releases are properly tagged and documented. ([`274e361`](https://github.com/ivansaul/test-semantic-release/commit/274e361bf951791c8742fcf1ca0e7127d71c83eb))

* fix: remove commit author from `semantic-release`

The `semantic-release` configuration is adjusted to remove the commit author field. This change ensures that the release process is standardized and prevents potential issues related to commit author information. ([`d1fedba`](https://github.com/ivansaul/test-semantic-release/commit/d1fedba074b4d816933986462b469febabc94fc5))

### Unknown

* Merge pull request #1 from ivansaul/feature/semantic-release

feat: add feature/semantic release ([`8aaa4ce`](https://github.com/ivansaul/test-semantic-release/commit/8aaa4ce0bdac4a657fc4381b03e0edf06e6e6163))

* Fix: remove unnecessary `-D` flag

The `-D` flag in the `semantic-release publish` command is redundant, as it defaults to using the provided `commit_author`. This change removes the flag for clarity and consistency. ([`86df57b`](https://github.com/ivansaul/test-semantic-release/commit/86df57b7cb20e25710d6f0ed7f54fbd859375103))

* Initial commit ([`f9e5490`](https://github.com/ivansaul/test-semantic-release/commit/f9e54901993922ee59c3074a11997ab31e1f650b))

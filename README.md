# Images And The Asset Pipeline

## Objectives

1. Add images to the Rails Asset Pipeline
2. Construct image asset URLs.
3. Use asset_path and asset_url helpers.
4. Use image_tag helpers

## Instructions

Where do images go?

app/assets/images is in the asset paths and you could add different image directories paths to the asset paths via Rails.application.assets.paths array. Once there we treat these assets as any other asset, simply linking them via the magic /assets URL.

The goal is to sort of demonstrate the differences in:
https://dl.dropboxusercontent.com/s/wyernhisw06nrn5/2016-01-19%20at%208.58%20PM.png

we're trying to show them the differences between the following asset/image helpers:

asset_path (when an asset is found vs when it isn't)
image_tag (when the asset is found vs when it isnt)

Have them predict asset path urls for files in different directories, show them how that pattern works by constructing their own valid asset URLs.

generate those urls with fingerprints via the asset_path helper that all other asset loads will use (javascript_include_tag uses that internally...)

note the danger in using <img src=> and manually trying to guess the asset url and not getting the fingerprint.

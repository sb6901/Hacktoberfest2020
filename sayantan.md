# This is a basic workflow to help you get started with Actions
name: CI
# Controls when the action will run. Triggers the workflow on push or pull request
# events but only for the master branch
on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]
# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest
    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v2
      # Runs a single command using the runners shell
      - name: Run a one-line script
        run: echo Hello, world!
      # Runs a set of commands using the runners shell
      - name: Run a multi-line script
        run: |
          echo Add other actions to build,
          echo test, and deploy your project.
          
      - name: Image Actions
  # You may pin to the exact commit or the version.
  # uses: calibreapp/image-actions@737ceeaeed61e17b8d358358a303f1b8d177b779
  uses: calibreapp/image-actions@1.1.0
  with:
    # GitHub Token
    githubToken: 
    # JPEG quality level
    jpegQuality: # optional, default is 80
    # PNG quality level
    pngQuality: # optional, default is 80
    # WEBP quality level
    webpQuality: # optional, default is 80
    # Paths to ignore during search
    ignorePaths: # optional, default is node_modules/**


- name: Image Optimizer
  # You may pin to the exact commit or the version.
  # uses: crush-pics/crush-pics-github-action@43ce9e319a61c10d7438da324515336caee56492
  uses: crush-pics/crush-pics-github-action@v1.0

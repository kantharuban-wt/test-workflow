# test-workflow
act workflow_dispatch -j build --input environment="SIT" --input service="cm" -P windows-latest=mcr.microsoft.com/windows/servercore:ltsc2022

act workflow_dispatch -j build --input environment="SIT" --input service="cm" -P windows-latest=-self-hosted

act -j build  -P windows-latest=mcr.microsoft.com/windows/servercore:ltsc2022

act -j build  -P windows-latest=-self-hosted




act workflow_dispatch -W .github/workflows/main.yml --input environment="SIT" --input service="cm" -P windows-latest=-self-hosted
node {
    stage "Create build output"
    sh "mkdir -p output"
    writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."
    writeFile file: "output/uselessfile.md", text: "This file is useless, no need to archive it."
    stage "Archive build output"
    archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'
}

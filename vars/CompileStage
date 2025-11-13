def call() {

    echo "======================================"
    echo "        🔧 Compile Stage Started      "
    echo "======================================"

    try {
        sh "mvn clean compile"

        echo "======================================"
        echo "      ✅ Compile Completed Successfully"
        echo "======================================"

    } catch (err) {

        echo "======================================"
        echo "      ❌ Compile Failed"
        echo "      Error: ${err}"
        echo "======================================"

        currentBuild.result = 'FAILURE'
        throw err   // stop pipeline
    }
}


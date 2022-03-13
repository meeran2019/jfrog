
---------------------------------------------------------------------------------------------------------
INTRODUCTION: 
---------------------------------------------------------------------------------------------------------

Source Code + Dependencies -> Binary (Build) -> Artifact (Package)

Artifactory: 
    A Universal Binary (blob file) repository manager. 
    Can store all artifacts and dependencies. 
    Proxy for remote repositories like npm etc (Dependcies are stored in jfrog as cache)
    It act as both resolve dependencies throughcache and store built artifacts. 

Why Artifactory: 
    Universal - Integrate with multiple package managers and CI servers. 
    System of Record - Full metadata for all supported package formats. Captures artifact information.
    Storage Optimization - Checksum based storage. 
    Automation - Rest API, CLI, User plugins. 
    Integration - Built in integration with automation tools for CI/CD. 
    It supports docker can store and distribute docker images. 
    It supports Chef. 

Repository: 
    Local: 
        Physical, local
        Produce and consume artifacts 
        Artifacts under a local repository are directly accessible via URL pattern of 
                http://host:port/artifactory/local-repository-name/artifact-path 

    Remote: 
        Serves a caching proxy of another network repository.
        can remove cached artifacts but cannot deploy manually deploy. 
        Artifacts under remore repository are directly accessible via URL pattern of 
                http://hosts:port/artifactory/remote-repository-name/artifact-path

    Virtual: 
        It aggregates several repositories under a common URL.
        can resolve and get artifacts but cannot deploy anything. 

        Local repo (first)  -> Remote repo cache -> Remote repo (last) 

---------------------------------------------------------------------------------------------------------

INSTALLATION: 

    https://computingforgeeks.com/how-to-install-jfrog-artifactory-on-ubuntu/

    http://localhost:8081/artifactory/

    Username/Password - admin/password
    
---------------------------------------------------------------------------------------------------------








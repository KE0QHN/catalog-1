---
hide:
  - toc
---

# Security Overview

<link href="https://truecharts.org/_static/trivy.css" type="text/css" rel="stylesheet" />

## Helm-Chart

##### Scan Results

#### Chart Object: pgadmin/templates/common.yaml



| Type         |    Misconfiguration ID   |   Check  |  Severity |                   Explaination                   | Links  |
|:----------------|:------------------:|:-----------:|:------------------:|-----------------------------------------|-----------------------------------------|
| Kubernetes Security Check         |    KSV001   |   Process can elevate its own privileges  |  MEDIUM | <details><summary>Expand...</summary> A program inside the container can elevate its own privileges and run as root, which might give the program control over the container and node. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.allowPrivilegeEscalation&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv001">https://avd.aquasec.com/appshield/ksv001</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;RELEASE-NAME-pgadmin&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV011   |   CPU not limited  |  LOW | <details><summary>Expand...</summary> Enforcing CPU limits prevents DoS via resource exhaustion. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;resources.limits.cpu&#39; </details>| <details><summary>Expand...</summary><a href="https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits">https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits</a><br><a href="https://avd.aquasec.com/appshield/ksv011">https://avd.aquasec.com/appshield/ksv011</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;RELEASE-NAME-pgadmin&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;RELEASE-NAME-pgadmin&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV015   |   CPU requests not specified  |  LOW | <details><summary>Expand...</summary> When containers have resource requests specified, the scheduler can make better decisions about which nodes to place pods on, and how to deal with resource contention. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;resources.requests.cpu&#39; </details>| <details><summary>Expand...</summary><a href="https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits">https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits</a><br><a href="https://avd.aquasec.com/appshield/ksv015">https://avd.aquasec.com/appshield/ksv015</a><br></details>  |
| Kubernetes Security Check         |    KSV016   |   Memory requests not specified  |  LOW | <details><summary>Expand...</summary> When containers have memory requests specified, the scheduler can make better decisions about which nodes to place pods on, and how to deal with resource contention. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;resources.requests.memory&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-resources-limits-memory/">https://kubesec.io/basics/containers-resources-limits-memory/</a><br><a href="https://avd.aquasec.com/appshield/ksv016">https://avd.aquasec.com/appshield/ksv016</a><br></details>  |
| Kubernetes Security Check         |    KSV017   |   Privileged container  |  HIGH | <details><summary>Expand...</summary> Privileged containers share namespaces with the host system and do not offer any security. They should be used exclusively for system containers that require high privileges. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.privileged&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv017">https://avd.aquasec.com/appshield/ksv017</a><br></details>  |
| Kubernetes Security Check         |    KSV018   |   Memory not limited  |  LOW | <details><summary>Expand...</summary> Enforcing memory limits prevents DoS via resource exhaustion. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;resources.limits.memory&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-resources-limits-memory/">https://kubesec.io/basics/containers-resources-limits-memory/</a><br><a href="https://avd.aquasec.com/appshield/ksv018">https://avd.aquasec.com/appshield/ksv018</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-pgadmin&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-pgadmin&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV023   |   hostPath volumes mounted  |  MEDIUM | <details><summary>Expand...</summary> HostPath volumes must be forbidden. <br> <hr> <br> Deployment &#39;RELEASE-NAME-pgadmin&#39; should not set &#39;spec.template.volumes.hostPath&#39; </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv023">https://avd.aquasec.com/appshield/ksv023</a><br></details>  |
| Kubernetes Security Check         |    KSV029   |   A root primary or supplementary GID set  |  LOW | <details><summary>Expand...</summary> Containers should be forbidden from running with a root primary or supplementary GID. <br> <hr> <br> Deployment &#39;RELEASE-NAME-pgadmin&#39; should set &#39;spec.securityContext.runAsGroup&#39;, &#39;spec.securityContext.supplementalGroups[*]&#39; and &#39;spec.securityContext.fsGroup&#39; to integer greater than 0 </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv029">https://avd.aquasec.com/appshield/ksv029</a><br></details>  |

## Containers

##### Detected Containers

          tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583
          tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583
          tccr.io/truecharts/pgadmin4:v6.7@sha256:c187b358389e145be5c20b6773abbca1d86af7ff4c6406fb325a7373f1455326

##### Scan Results


#### Container: tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583 (alpine 3.15.2)


**alpine**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| zlib         |    CVE-2018-25032   |   HIGH  |  1.2.11-r3 | 1.2.12-r0 | <details><summary>Expand...</summary><a href="http://www.openwall.com/lists/oss-security/2022/03/25/2">http://www.openwall.com/lists/oss-security/2022/03/25/2</a><br><a href="http://www.openwall.com/lists/oss-security/2022/03/26/1">http://www.openwall.com/lists/oss-security/2022/03/26/1</a><br><a href="https://access.redhat.com/security/cve/CVE-2018-25032">https://access.redhat.com/security/cve/CVE-2018-25032</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032</a><br><a href="https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531">https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531</a><br><a href="https://github.com/madler/zlib/compare/v1.2.11...v1.2.12">https://github.com/madler/zlib/compare/v1.2.11...v1.2.12</a><br><a href="https://github.com/madler/zlib/issues/605">https://github.com/madler/zlib/issues/605</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html">https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2018-25032">https://nvd.nist.gov/vuln/detail/CVE-2018-25032</a><br><a href="https://ubuntu.com/security/notices/USN-5355-1">https://ubuntu.com/security/notices/USN-5355-1</a><br><a href="https://ubuntu.com/security/notices/USN-5355-2">https://ubuntu.com/security/notices/USN-5355-2</a><br><a href="https://ubuntu.com/security/notices/USN-5359-1">https://ubuntu.com/security/notices/USN-5359-1</a><br><a href="https://www.debian.org/security/2022/dsa-5111">https://www.debian.org/security/2022/dsa-5111</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/24/1">https://www.openwall.com/lists/oss-security/2022/03/24/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/1">https://www.openwall.com/lists/oss-security/2022/03/28/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/3">https://www.openwall.com/lists/oss-security/2022/03/28/3</a><br></details>  |


#### Container: tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583 (alpine 3.15.2)


**alpine**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| zlib         |    CVE-2018-25032   |   HIGH  |  1.2.11-r3 | 1.2.12-r0 | <details><summary>Expand...</summary><a href="http://www.openwall.com/lists/oss-security/2022/03/25/2">http://www.openwall.com/lists/oss-security/2022/03/25/2</a><br><a href="http://www.openwall.com/lists/oss-security/2022/03/26/1">http://www.openwall.com/lists/oss-security/2022/03/26/1</a><br><a href="https://access.redhat.com/security/cve/CVE-2018-25032">https://access.redhat.com/security/cve/CVE-2018-25032</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032</a><br><a href="https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531">https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531</a><br><a href="https://github.com/madler/zlib/compare/v1.2.11...v1.2.12">https://github.com/madler/zlib/compare/v1.2.11...v1.2.12</a><br><a href="https://github.com/madler/zlib/issues/605">https://github.com/madler/zlib/issues/605</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html">https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2018-25032">https://nvd.nist.gov/vuln/detail/CVE-2018-25032</a><br><a href="https://ubuntu.com/security/notices/USN-5355-1">https://ubuntu.com/security/notices/USN-5355-1</a><br><a href="https://ubuntu.com/security/notices/USN-5355-2">https://ubuntu.com/security/notices/USN-5355-2</a><br><a href="https://ubuntu.com/security/notices/USN-5359-1">https://ubuntu.com/security/notices/USN-5359-1</a><br><a href="https://www.debian.org/security/2022/dsa-5111">https://www.debian.org/security/2022/dsa-5111</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/24/1">https://www.openwall.com/lists/oss-security/2022/03/24/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/1">https://www.openwall.com/lists/oss-security/2022/03/28/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/3">https://www.openwall.com/lists/oss-security/2022/03/28/3</a><br></details>  |


#### Container: tccr.io/truecharts/pgadmin4:v6.7@sha256:c187b358389e145be5c20b6773abbca1d86af7ff4c6406fb325a7373f1455326 (alpine 3.15.0)


**alpine**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| krb5-libs         |    CVE-2021-37750   |   MEDIUM  |  1.19.2-r4 | 1.19.3-r0 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2021-37750">https://access.redhat.com/security/cve/CVE-2021-37750</a><br><a href="https://github.com/krb5/krb5/commit/d775c95af7606a51bf79547a94fa52ddd1cb7f49">https://github.com/krb5/krb5/commit/d775c95af7606a51bf79547a94fa52ddd1cb7f49</a><br><a href="https://github.com/krb5/krb5/releases">https://github.com/krb5/krb5/releases</a><br><a href="https://linux.oracle.com/cve/CVE-2021-37750.html">https://linux.oracle.com/cve/CVE-2021-37750.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2021-4788.html">https://linux.oracle.com/errata/ELSA-2021-4788.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2021/09/msg00019.html">https://lists.debian.org/debian-lts-announce/2021/09/msg00019.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/MFCLW7D46E4VCREKKH453T5DA4XOLHU2/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/MFCLW7D46E4VCREKKH453T5DA4XOLHU2/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2021-37750">https://nvd.nist.gov/vuln/detail/CVE-2021-37750</a><br><a href="https://security.netapp.com/advisory/ntap-20210923-0002/">https://security.netapp.com/advisory/ntap-20210923-0002/</a><br><a href="https://web.mit.edu/kerberos/advisories/">https://web.mit.edu/kerberos/advisories/</a><br></details>  |
| libcrypto1.1         |    CVE-2022-0778   |   HIGH  |  1.1.1l-r7 | 1.1.1n-r0 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2022-0778">https://access.redhat.com/security/cve/CVE-2022-0778</a><br><a href="https://crates.io/crates/openssl-src">https://crates.io/crates/openssl-src</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=3118eb64934499d93db3230748a452351d1d9a65">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=3118eb64934499d93db3230748a452351d1d9a65</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=380085481c64de749a6dd25cdf0bcf4360b30f83">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=380085481c64de749a6dd25cdf0bcf4360b30f83</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=a466912611aa6cbdf550cd10601390e587451246">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=a466912611aa6cbdf550cd10601390e587451246</a><br><a href="https://linux.oracle.com/cve/CVE-2022-0778.html">https://linux.oracle.com/cve/CVE-2022-0778.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2022-9258.html">https://linux.oracle.com/errata/ELSA-2022-9258.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00023.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00023.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00024.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00024.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/323SNN6ZX7PRJJWP2BUAFLPUAE42XWLZ/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/323SNN6ZX7PRJJWP2BUAFLPUAE42XWLZ/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/GDB3GQVJPXJE7X5C5JN6JAA4XUDWD6E6/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/GDB3GQVJPXJE7X5C5JN6JAA4XUDWD6E6/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-0778">https://nvd.nist.gov/vuln/detail/CVE-2022-0778</a><br><a href="https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2022-0002">https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2022-0002</a><br><a href="https://rustsec.org/advisories/RUSTSEC-2022-0014.html">https://rustsec.org/advisories/RUSTSEC-2022-0014.html</a><br><a href="https://security.netapp.com/advisory/ntap-20220321-0002/">https://security.netapp.com/advisory/ntap-20220321-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5328-1">https://ubuntu.com/security/notices/USN-5328-1</a><br><a href="https://ubuntu.com/security/notices/USN-5328-2">https://ubuntu.com/security/notices/USN-5328-2</a><br><a href="https://www.debian.org/security/2022/dsa-5103">https://www.debian.org/security/2022/dsa-5103</a><br><a href="https://www.openssl.org/news/secadv/20220315.txt">https://www.openssl.org/news/secadv/20220315.txt</a><br><a href="https://www.tenable.com/security/tns-2022-06">https://www.tenable.com/security/tns-2022-06</a><br><a href="https://www.tenable.com/security/tns-2022-07">https://www.tenable.com/security/tns-2022-07</a><br></details>  |
| libretls         |    CVE-2022-0778   |   HIGH  |  3.3.4-r2 | 3.3.4-r3 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2022-0778">https://access.redhat.com/security/cve/CVE-2022-0778</a><br><a href="https://crates.io/crates/openssl-src">https://crates.io/crates/openssl-src</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=3118eb64934499d93db3230748a452351d1d9a65">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=3118eb64934499d93db3230748a452351d1d9a65</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=380085481c64de749a6dd25cdf0bcf4360b30f83">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=380085481c64de749a6dd25cdf0bcf4360b30f83</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=a466912611aa6cbdf550cd10601390e587451246">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=a466912611aa6cbdf550cd10601390e587451246</a><br><a href="https://linux.oracle.com/cve/CVE-2022-0778.html">https://linux.oracle.com/cve/CVE-2022-0778.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2022-9258.html">https://linux.oracle.com/errata/ELSA-2022-9258.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00023.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00023.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00024.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00024.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/323SNN6ZX7PRJJWP2BUAFLPUAE42XWLZ/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/323SNN6ZX7PRJJWP2BUAFLPUAE42XWLZ/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/GDB3GQVJPXJE7X5C5JN6JAA4XUDWD6E6/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/GDB3GQVJPXJE7X5C5JN6JAA4XUDWD6E6/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-0778">https://nvd.nist.gov/vuln/detail/CVE-2022-0778</a><br><a href="https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2022-0002">https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2022-0002</a><br><a href="https://rustsec.org/advisories/RUSTSEC-2022-0014.html">https://rustsec.org/advisories/RUSTSEC-2022-0014.html</a><br><a href="https://security.netapp.com/advisory/ntap-20220321-0002/">https://security.netapp.com/advisory/ntap-20220321-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5328-1">https://ubuntu.com/security/notices/USN-5328-1</a><br><a href="https://ubuntu.com/security/notices/USN-5328-2">https://ubuntu.com/security/notices/USN-5328-2</a><br><a href="https://www.debian.org/security/2022/dsa-5103">https://www.debian.org/security/2022/dsa-5103</a><br><a href="https://www.openssl.org/news/secadv/20220315.txt">https://www.openssl.org/news/secadv/20220315.txt</a><br><a href="https://www.tenable.com/security/tns-2022-06">https://www.tenable.com/security/tns-2022-06</a><br><a href="https://www.tenable.com/security/tns-2022-07">https://www.tenable.com/security/tns-2022-07</a><br></details>  |
| libsasl         |    CVE-2022-24407   |   HIGH  |  2.1.27-r14 | 2.1.28-r0 | <details><summary>Expand...</summary><a href="http://www.openwall.com/lists/oss-security/2022/02/23/4">http://www.openwall.com/lists/oss-security/2022/02/23/4</a><br><a href="https://access.redhat.com/security/cve/CVE-2022-24407">https://access.redhat.com/security/cve/CVE-2022-24407</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-24407">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-24407</a><br><a href="https://github.com/cyrusimap/cyrus-sasl/blob/fdcd13ceaef8de684dc69008011fa865c5b4a3ac/docsrc/sasl/release-notes/2.1/index.rst">https://github.com/cyrusimap/cyrus-sasl/blob/fdcd13ceaef8de684dc69008011fa865c5b4a3ac/docsrc/sasl/release-notes/2.1/index.rst</a><br><a href="https://linux.oracle.com/cve/CVE-2022-24407.html">https://linux.oracle.com/cve/CVE-2022-24407.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2022-9239.html">https://linux.oracle.com/errata/ELSA-2022-9239.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00002.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00002.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/4FIXU75Q6RBNK6UYM7MQ3TCFGXR7AX4U/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/4FIXU75Q6RBNK6UYM7MQ3TCFGXR7AX4U/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/H26R4SMGM3WHXX4XYNNJB4YGFIL5UNF4/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/H26R4SMGM3WHXX4XYNNJB4YGFIL5UNF4/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/ZZC6BMPI3V3MC2IGNLN377ETUWO7QBIH/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/ZZC6BMPI3V3MC2IGNLN377ETUWO7QBIH/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-24407">https://nvd.nist.gov/vuln/detail/CVE-2022-24407</a><br><a href="https://ubuntu.com/security/notices/USN-5301-1">https://ubuntu.com/security/notices/USN-5301-1</a><br><a href="https://ubuntu.com/security/notices/USN-5301-2">https://ubuntu.com/security/notices/USN-5301-2</a><br><a href="https://www.cyrusimap.org/sasl/sasl/release-notes/2.1/index.html#new-in-2-1-28">https://www.cyrusimap.org/sasl/sasl/release-notes/2.1/index.html#new-in-2-1-28</a><br><a href="https://www.debian.org/security/2022/dsa-5087">https://www.debian.org/security/2022/dsa-5087</a><br></details>  |
| libssl1.1         |    CVE-2022-0778   |   HIGH  |  1.1.1l-r7 | 1.1.1n-r0 | <details><summary>Expand...</summary><a href="https://access.redhat.com/security/cve/CVE-2022-0778">https://access.redhat.com/security/cve/CVE-2022-0778</a><br><a href="https://crates.io/crates/openssl-src">https://crates.io/crates/openssl-src</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-0778</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=3118eb64934499d93db3230748a452351d1d9a65">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=3118eb64934499d93db3230748a452351d1d9a65</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=380085481c64de749a6dd25cdf0bcf4360b30f83">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=380085481c64de749a6dd25cdf0bcf4360b30f83</a><br><a href="https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=a466912611aa6cbdf550cd10601390e587451246">https://git.openssl.org/gitweb/?p=openssl.git;a=commitdiff;h=a466912611aa6cbdf550cd10601390e587451246</a><br><a href="https://linux.oracle.com/cve/CVE-2022-0778.html">https://linux.oracle.com/cve/CVE-2022-0778.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2022-9258.html">https://linux.oracle.com/errata/ELSA-2022-9258.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00023.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00023.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/03/msg00024.html">https://lists.debian.org/debian-lts-announce/2022/03/msg00024.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/323SNN6ZX7PRJJWP2BUAFLPUAE42XWLZ/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/323SNN6ZX7PRJJWP2BUAFLPUAE42XWLZ/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/GDB3GQVJPXJE7X5C5JN6JAA4XUDWD6E6/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/GDB3GQVJPXJE7X5C5JN6JAA4XUDWD6E6/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-0778">https://nvd.nist.gov/vuln/detail/CVE-2022-0778</a><br><a href="https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2022-0002">https://psirt.global.sonicwall.com/vuln-detail/SNWLID-2022-0002</a><br><a href="https://rustsec.org/advisories/RUSTSEC-2022-0014.html">https://rustsec.org/advisories/RUSTSEC-2022-0014.html</a><br><a href="https://security.netapp.com/advisory/ntap-20220321-0002/">https://security.netapp.com/advisory/ntap-20220321-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5328-1">https://ubuntu.com/security/notices/USN-5328-1</a><br><a href="https://ubuntu.com/security/notices/USN-5328-2">https://ubuntu.com/security/notices/USN-5328-2</a><br><a href="https://www.debian.org/security/2022/dsa-5103">https://www.debian.org/security/2022/dsa-5103</a><br><a href="https://www.openssl.org/news/secadv/20220315.txt">https://www.openssl.org/news/secadv/20220315.txt</a><br><a href="https://www.tenable.com/security/tns-2022-06">https://www.tenable.com/security/tns-2022-06</a><br><a href="https://www.tenable.com/security/tns-2022-07">https://www.tenable.com/security/tns-2022-07</a><br></details>  |
| zlib         |    CVE-2018-25032   |   HIGH  |  1.2.11-r3 | 1.2.12-r0 | <details><summary>Expand...</summary><a href="http://www.openwall.com/lists/oss-security/2022/03/25/2">http://www.openwall.com/lists/oss-security/2022/03/25/2</a><br><a href="http://www.openwall.com/lists/oss-security/2022/03/26/1">http://www.openwall.com/lists/oss-security/2022/03/26/1</a><br><a href="https://access.redhat.com/security/cve/CVE-2018-25032">https://access.redhat.com/security/cve/CVE-2018-25032</a><br><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-25032</a><br><a href="https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531">https://github.com/madler/zlib/commit/5c44459c3b28a9bd3283aaceab7c615f8020c531</a><br><a href="https://github.com/madler/zlib/compare/v1.2.11...v1.2.12">https://github.com/madler/zlib/compare/v1.2.11...v1.2.12</a><br><a href="https://github.com/madler/zlib/issues/605">https://github.com/madler/zlib/issues/605</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html">https://lists.debian.org/debian-lts-announce/2022/04/msg00000.html</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2018-25032">https://nvd.nist.gov/vuln/detail/CVE-2018-25032</a><br><a href="https://ubuntu.com/security/notices/USN-5355-1">https://ubuntu.com/security/notices/USN-5355-1</a><br><a href="https://ubuntu.com/security/notices/USN-5355-2">https://ubuntu.com/security/notices/USN-5355-2</a><br><a href="https://ubuntu.com/security/notices/USN-5359-1">https://ubuntu.com/security/notices/USN-5359-1</a><br><a href="https://www.debian.org/security/2022/dsa-5111">https://www.debian.org/security/2022/dsa-5111</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/24/1">https://www.openwall.com/lists/oss-security/2022/03/24/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/1">https://www.openwall.com/lists/oss-security/2022/03/28/1</a><br><a href="https://www.openwall.com/lists/oss-security/2022/03/28/3">https://www.openwall.com/lists/oss-security/2022/03/28/3</a><br></details>  |

**python-pkg**


| No Vulnerabilities found         |
|:---------------------------------|
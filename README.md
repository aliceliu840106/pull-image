# pull-image

####### on-IT-sandbox #######
image_list:
registry.gitlab.com/gitlab-org/build/cng/gitlab-toolbox-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-sidekiq-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-webservice-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-workhorse-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-pages
registry.gitlab.com/gitlab-org/build/cng/gitaly
registry.gitlab.com/gitlab-org/build/cng/gitlab-base

asia-east1-docker.pkg.dev/gpnr19prj0015isb-extl/gpae19afr0001isb/

command:
for i in `cat image_list`; do docker pull $i:v15.7.9; docker tag $i:v15.7.9 asia-east1-docker.pkg.dev/gpnr19prj0015isb-extl/gpae19afr0001isb/$i:v15.7.9; docker push asia-east1-docker.pkg.dev/gpnr19prj0015isb-extl/gpae19afr0001isb/$i:v15.7.9; done


registry.gitlab.com/security-products/brakeman:4
registry.gitlab.com/security-products/flawfinder:4
registry.gitlab.com/security-products/nodejs-scan:4
registry.gitlab.com/security-products/phpcs-security-audit:4
registry.gitlab.com/security-products/pmd-apex:4
registry.gitlab.com/security-products/semgrep:4
registry.gitlab.com/security-products/sobelow:4
registry.gitlab.com/security-products/spotbugs:4

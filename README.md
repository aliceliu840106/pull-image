# pull-image

####### on-IT-sandbox #######
image_list:
registry.gitlab.com/gitlab-org/build/cng/gitlab-toolbox-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-sidekiq-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-webservice-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-workhorse-ce
registry.gitlab.com/gitlab-org/build/cng/gitlab-pages
registry.gitlab.com/gitlab-org/build/cng/gitaly

asia-east1-docker.pkg.dev/gpnr19prj0015isb-extl/gpae19afr0001isb/

command:
for i in `cat image_list`; do docker pull $i:v15.7.9; docker tag $i:v15.7.9 asia-east1-docker.pkg.dev/gpnr19prj0015isb-extl/gpae19afr0001isb/$i:v15.7.9; docker push asia-east1-docker.pkg.dev/gpnr19prj0015isb-extl/gpae19afr0001isb/$i:v15.7.9; done


FROM quay.io/operator-framework/ansible-operator:master

COPY watches.yaml ${HOME}/watches.yaml

COPY playbook.yml ${HOME}/playbook.yml

RUN mkdir -p ${HOME}/.ansible/collections/ansible_collections/community/kubernetes \
 && curl -L https://github.com/ansible-collections/kubernetes/archive/master.tar.gz | tar --strip-components=1 -C ${HOME}/.ansible/collections/ansible_collections/community/kubernetes -xz

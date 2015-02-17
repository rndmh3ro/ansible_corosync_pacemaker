corosync_pacemaker
=========

Install and configure Corosync and Pacemaker on RHEL-systems.

Requirements
------------
none.

Role Variables
--------------
- a hosts-list with the names of the interfaces that communicate in the cluster:


 - ```hosts: [host1-admin-if, host2-admin-if]```

- the ringnumber:

 - ```ringnumber: 0```

- The first node on the cluster:

 - ``` first_node: "host1"```

Dependencies
------------
none.

Example Playbook
----------------

    - hosts: host1-admin-if:host2-admin-if
      gather_facts: True
      roles:
        - { role: corosync_pacemaker, hosts: [host1-admin-if,host2-admin-if], ringnumber: 0, first_node: "host1" }


License
-------

GPLv3

Author Information
------------------

Author: Sebastian Gumprich

Author: [T-Systems Multimedia Solutions GmbH](http://www.t-systems-mms.com/)


Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.


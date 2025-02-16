
<!-- markdownlint-disable -->
# terraform-opsgenie-incident-management

 [![Latest Release](https://img.shields.io/github/release/cloudposse/terraform-opsgenie-incident-management.svg)](https://github.com/cloudposse/terraform-opsgenie-incident-management/releases/latest) [![Slack Community](https://slack.cloudposse.com/badge.svg)](https://slack.cloudposse.com) [![Discourse Forum](https://img.shields.io/discourse/https/ask.sweetops.com/posts.svg)](https://ask.sweetops.com/)
<!-- markdownlint-restore -->

[![README Header][readme_header_img]][readme_header_link]

[![Cloud Posse][logo]](https://cpco.io/homepage)

<!--




  ** DO NOT EDIT THIS FILE
  **
  ** This file was automatically generated by the `build-harness`.
  ** 1) Make all changes to `README.yaml`
  ** 2) Run `make init` (you only need to do this once)
  ** 3) Run`make readme` to rebuild this file.
  **
  ** (We maintain HUNDREDS of open source projects. This is how we maintain our sanity.)
  **





-->

Terraform module to provision Opsgenie resources using the Opsgenie provider. The provider needs to be configured with the proper credentials before it can be used.
It consist of root module which is only here as an example but can be used as a combination of all submodules. Submodules can also be combined to abstract away complexity of setting up for example a team escalation.

---

This project is part of our comprehensive ["SweetOps"](https://cpco.io/sweetops) approach towards DevOps.
[<img align="right" title="Share via Email" src="https://docs.cloudposse.com/images/ionicons/ios-email-outline-2.0.1-16x16-999999.svg"/>][share_email]
[<img align="right" title="Share on Google+" src="https://docs.cloudposse.com/images/ionicons/social-googleplus-outline-2.0.1-16x16-999999.svg" />][share_googleplus]
[<img align="right" title="Share on Facebook" src="https://docs.cloudposse.com/images/ionicons/social-facebook-outline-2.0.1-16x16-999999.svg" />][share_facebook]
[<img align="right" title="Share on Reddit" src="https://docs.cloudposse.com/images/ionicons/social-reddit-outline-2.0.1-16x16-999999.svg" />][share_reddit]
[<img align="right" title="Share on LinkedIn" src="https://docs.cloudposse.com/images/ionicons/social-linkedin-outline-2.0.1-16x16-999999.svg" />][share_linkedin]
[<img align="right" title="Share on Twitter" src="https://docs.cloudposse.com/images/ionicons/social-twitter-outline-2.0.1-16x16-999999.svg" />][share_twitter]


[![Terraform Open Source Modules](https://docs.cloudposse.com/images/terraform-open-source-modules.svg)][terraform_modules]



It's 100% Open Source and licensed under the [APACHE2](LICENSE).







We literally have [*hundreds of terraform modules*][terraform_modules] that are Open Source and well-maintained. Check them out!





## Introduction

Available modules:
- [Alert Policy](modules/alert_policy)
- [API Integration](modules/api_integration)
- [Config](modules/config)
- [Escalation](modules/escalation)
- [Integration Action](modules/integration_action) (advanced feature — not available to all OpsGenie plans)
- [Notification Policy](modules/notification_policy)
- [Team](modules/team)
- [Team Routing Rule](modules/team_routing_rule)
- [User](modules/user)
- [Service](modules/service)
- [Service Incident Rule](modules/service_incident_rule)

**Note:** Root module is just an example that uses all of submodules.

**Note:** See the [Advanced Features Example](examples/advanced_features) for features only available to some OpsGenie plans.


## Security & Compliance [<img src="https://cloudposse.com/wp-content/uploads/2020/11/bridgecrew.svg" width="250" align="right" />](https://bridgecrew.io/)

Security scanning is graciously provided by Bridgecrew. Bridgecrew is the leading fully hosted, cloud-native solution providing continuous Terraform security and compliance.

| Benchmark | Description |
|--------|---------------|
| [![Infrastructure Security](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/general)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=INFRASTRUCTURE+SECURITY) | Infrastructure Security Compliance |
| [![CIS KUBERNETES](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/cis_kubernetes)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=CIS+KUBERNETES+V1.5) | Center for Internet Security, KUBERNETES Compliance |
| [![CIS AWS](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/cis_aws)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=CIS+AWS+V1.2) | Center for Internet Security, AWS Compliance |
| [![CIS AZURE](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/cis_azure)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=CIS+AZURE+V1.1) | Center for Internet Security, AZURE Compliance |
| [![PCI-DSS](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/pci)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=PCI-DSS+V3.2) | Payment Card Industry Data Security Standards Compliance |
| [![NIST-800-53](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/nist)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=NIST-800-53) | National Institute of Standards and Technology Compliance |
| [![ISO27001](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/iso)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=ISO27001) | Information Security Management System, ISO/IEC 27001 Compliance |
| [![SOC2](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/soc2)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=SOC2)| Service Organization Control 2 Compliance |
| [![CIS GCP](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/cis_gcp)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=CIS+GCP+V1.1) | Center for Internet Security, GCP Compliance |
| [![HIPAA](https://www.bridgecrew.cloud/badges/github/cloudposse/terraform-opsgenie-incident-management/hipaa)](https://www.bridgecrew.cloud/link/badge?vcs=github&fullRepo=cloudposse%2Fterraform-opsgenie-incident-management&benchmark=HIPAA) | Health Insurance Portability and Accountability Compliance |



## Usage


**IMPORTANT:** We do not pin modules to versions in our examples because of the
difficulty of keeping the versions in the documentation in sync with the latest released versions.
We highly recommend that in your code you pin the version to the exact version you are
using so that your infrastructure remains stable, and update versions in a
systematic way so that they do not catch you by surprise.

Also, because of a bug in the Terraform registry ([hashicorp/terraform#21417](https://github.com/hashicorp/terraform/issues/21417)),
the registry shows many of our inputs as required when in fact they are optional.
The table below correctly indicates which inputs are required.


Here's how to invoke `team` module in your projects

```hcl
module "team-name" {
  source  = "cloudposse/incident-management/opsgenie//modules/team"
  # Cloud Posse recommends pinning every module to a specific version
  # version     = "x.x.x"

  team = {
    name        = "team-name"
    description = "team-description"
  }
}
```




## Examples

Here are examples of using the module:

- [`complete`](examples/complete) - complete example of using this module

Submodules examples:
- [`alert_policy`](examples/alert_policy)
- [`api_integration`](examples/api_integration)
- [`escalation`](examples/escalation)
- [`integration_action`](examples/integration_action) (advanced feature — not available to all OpsGenie plans)
- [`notification_policy`](examples/notification_policy)
- [`team`](examples/team)
- [`team_routing_rule`](examples/team_routing_rule)
- [`user`](examples/user)

Here is an example of using the `config` module, which incorporates all resource declarations into a single module:
- [`config`](examples/config)

Here are automated tests for the examples using [bats](https://github.com/bats-core/bats-core) and [Terratest](https://github.com/gruntwork-io/terratest) (which tests and provisions the examples):
 - [test](test)



<!-- markdownlint-disable -->
## Makefile Targets
```text
Available targets:

  help                                Help screen
  help/all                            Display help for all targets
  help/short                          This help short screen
  lint                                Lint terraform code

```
<!-- markdownlint-restore -->
<!-- markdownlint-disable -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.13.0 |
| <a name="requirement_opsgenie"></a> [opsgenie](#requirement\_opsgenie) | >= 0.4 |

## Providers

No providers.

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_alert_policy"></a> [alert\_policy](#module\_alert\_policy) | ./modules/alert_policy | n/a |
| <a name="module_api_integration"></a> [api\_integration](#module\_api\_integration) | ./modules/api_integration | n/a |
| <a name="module_escalation"></a> [escalation](#module\_escalation) | ./modules/escalation | n/a |
| <a name="module_integration_action"></a> [integration\_action](#module\_integration\_action) | ./modules/integration_action | n/a |
| <a name="module_notification_policy"></a> [notification\_policy](#module\_notification\_policy) | ./modules/notification_policy | n/a |
| <a name="module_service"></a> [service](#module\_service) | ./modules/service | n/a |
| <a name="module_service_incident_rule"></a> [service\_incident\_rule](#module\_service\_incident\_rule) | ./modules/service_incident_rule | n/a |
| <a name="module_team"></a> [team](#module\_team) | ./modules/team | n/a |
| <a name="module_team_routing_rule"></a> [team\_routing\_rule](#module\_team\_routing\_rule) | ./modules/team_routing_rule | n/a |
| <a name="module_this"></a> [this](#module\_this) | cloudposse/label/null | 0.25.0 |
| <a name="module_user"></a> [user](#module\_user) | ./modules/user | n/a |

## Resources

No resources.

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_additional_tag_map"></a> [additional\_tag\_map](#input\_additional\_tag\_map) | Additional key-value pairs to add to each map in `tags_as_list_of_maps`. Not added to `tags` or `id`.<br>This is for some rare cases where resources want additional configuration of tags<br>and therefore take a list of maps with tag key, value, and additional configuration. | `map(string)` | `{}` | no |
| <a name="input_alert_policy"></a> [alert\_policy](#input\_alert\_policy) | Opsgenie Alert Policy configuration | `map` | `{}` | no |
| <a name="input_api_integration"></a> [api\_integration](#input\_api\_integration) | Opsgenie API Integration configuration | `map` | `{}` | no |
| <a name="input_attributes"></a> [attributes](#input\_attributes) | ID element. Additional attributes (e.g. `workers` or `cluster`) to add to `id`,<br>in the order they appear in the list. New attributes are appended to the<br>end of the list. The elements of the list are joined by the `delimiter`<br>and treated as a single ID element. | `list(string)` | `[]` | no |
| <a name="input_context"></a> [context](#input\_context) | Single object for setting entire context at once.<br>See description of individual variables for details.<br>Leave string and numeric variables as `null` to use default value.<br>Individual variable settings (non-null) override settings in context object,<br>except for attributes, tags, and additional\_tag\_map, which are merged. | `any` | <pre>{<br>  "additional_tag_map": {},<br>  "attributes": [],<br>  "delimiter": null,<br>  "descriptor_formats": {},<br>  "enabled": true,<br>  "environment": null,<br>  "id_length_limit": null,<br>  "label_key_case": null,<br>  "label_order": [],<br>  "label_value_case": null,<br>  "labels_as_tags": [<br>    "unset"<br>  ],<br>  "name": null,<br>  "namespace": null,<br>  "regex_replace_chars": null,<br>  "stage": null,<br>  "tags": {},<br>  "tenant": null<br>}</pre> | no |
| <a name="input_delimiter"></a> [delimiter](#input\_delimiter) | Delimiter to be used between ID elements.<br>Defaults to `-` (hyphen). Set to `""` to use no delimiter at all. | `string` | `null` | no |
| <a name="input_descriptor_formats"></a> [descriptor\_formats](#input\_descriptor\_formats) | Describe additional descriptors to be output in the `descriptors` output map.<br>Map of maps. Keys are names of descriptors. Values are maps of the form<br>`{<br>   format = string<br>   labels = list(string)<br>}`<br>(Type is `any` so the map values can later be enhanced to provide additional options.)<br>`format` is a Terraform format string to be passed to the `format()` function.<br>`labels` is a list of labels, in order, to pass to `format()` function.<br>Label values will be normalized before being passed to `format()` so they will be<br>identical to how they appear in `id`.<br>Default is `{}` (`descriptors` output will be empty). | `any` | `{}` | no |
| <a name="input_enabled"></a> [enabled](#input\_enabled) | Set to false to prevent the module from creating any resources | `bool` | `null` | no |
| <a name="input_environment"></a> [environment](#input\_environment) | ID element. Usually used for region e.g. 'uw2', 'us-west-2', OR role 'prod', 'staging', 'dev', 'UAT' | `string` | `null` | no |
| <a name="input_escalation"></a> [escalation](#input\_escalation) | Opsgenie Escalation configuration | `map` | `{}` | no |
| <a name="input_id_length_limit"></a> [id\_length\_limit](#input\_id\_length\_limit) | Limit `id` to this many characters (minimum 6).<br>Set to `0` for unlimited length.<br>Set to `null` for keep the existing setting, which defaults to `0`.<br>Does not affect `id_full`. | `number` | `null` | no |
| <a name="input_integration_action"></a> [integration\_action](#input\_integration\_action) | Opsgenie Integration Action configuration | `map` | `{}` | no |
| <a name="input_label_key_case"></a> [label\_key\_case](#input\_label\_key\_case) | Controls the letter case of the `tags` keys (label names) for tags generated by this module.<br>Does not affect keys of tags passed in via the `tags` input.<br>Possible values: `lower`, `title`, `upper`.<br>Default value: `title`. | `string` | `null` | no |
| <a name="input_label_order"></a> [label\_order](#input\_label\_order) | The order in which the labels (ID elements) appear in the `id`.<br>Defaults to ["namespace", "environment", "stage", "name", "attributes"].<br>You can omit any of the 6 labels ("tenant" is the 6th), but at least one must be present. | `list(string)` | `null` | no |
| <a name="input_label_value_case"></a> [label\_value\_case](#input\_label\_value\_case) | Controls the letter case of ID elements (labels) as included in `id`,<br>set as tag values, and output by this module individually.<br>Does not affect values of tags passed in via the `tags` input.<br>Possible values: `lower`, `title`, `upper` and `none` (no transformation).<br>Set this to `title` and set `delimiter` to `""` to yield Pascal Case IDs.<br>Default value: `lower`. | `string` | `null` | no |
| <a name="input_labels_as_tags"></a> [labels\_as\_tags](#input\_labels\_as\_tags) | Set of labels (ID elements) to include as tags in the `tags` output.<br>Default is to include all labels.<br>Tags with empty values will not be included in the `tags` output.<br>Set to `[]` to suppress all generated tags.<br>**Notes:**<br>  The value of the `name` tag, if included, will be the `id`, not the `name`.<br>  Unlike other `null-label` inputs, the initial setting of `labels_as_tags` cannot be<br>  changed in later chained modules. Attempts to change it will be silently ignored. | `set(string)` | <pre>[<br>  "default"<br>]</pre> | no |
| <a name="input_name"></a> [name](#input\_name) | ID element. Usually the component or solution name, e.g. 'app' or 'jenkins'.<br>This is the only ID element not also included as a `tag`.<br>The "name" tag is set to the full `id` string. There is no tag with the value of the `name` input. | `string` | `null` | no |
| <a name="input_namespace"></a> [namespace](#input\_namespace) | ID element. Usually an abbreviation of your organization name, e.g. 'eg' or 'cp', to help ensure generated IDs are globally unique | `string` | `null` | no |
| <a name="input_notification_policy"></a> [notification\_policy](#input\_notification\_policy) | Opsgenie Notification Policy configuration | `map` | `{}` | no |
| <a name="input_opsgenie_provider_api_key"></a> [opsgenie\_provider\_api\_key](#input\_opsgenie\_provider\_api\_key) | The API Key for the Opsgenie Integration. If omitted, the OPSGENIE\_API\_KEY environment variable is used | `string` | `""` | no |
| <a name="input_regex_replace_chars"></a> [regex\_replace\_chars](#input\_regex\_replace\_chars) | Terraform regular expression (regex) string.<br>Characters matching the regex will be removed from the ID elements.<br>If not set, `"/[^a-zA-Z0-9-]/"` is used to remove all characters other than hyphens, letters and digits. | `string` | `null` | no |
| <a name="input_service"></a> [service](#input\_service) | Opsgenie Service configuration | `map` | `{}` | no |
| <a name="input_service_incident_rule"></a> [service\_incident\_rule](#input\_service\_incident\_rule) | Opsgenie Service Incident Rule configuration | `map` | `{}` | no |
| <a name="input_stage"></a> [stage](#input\_stage) | ID element. Usually used to indicate role, e.g. 'prod', 'staging', 'source', 'build', 'test', 'deploy', 'release' | `string` | `null` | no |
| <a name="input_tags"></a> [tags](#input\_tags) | Additional tags (e.g. `{'BusinessUnit': 'XYZ'}`).<br>Neither the tag keys nor the tag values will be modified by this module. | `map(string)` | `{}` | no |
| <a name="input_team"></a> [team](#input\_team) | Opsgenie Team configuration | `map` | `{}` | no |
| <a name="input_team_routing_rule"></a> [team\_routing\_rule](#input\_team\_routing\_rule) | Opsgenie Team Routing Rule configuration | `map` | `{}` | no |
| <a name="input_tenant"></a> [tenant](#input\_tenant) | ID element \_(Rarely used, not included by default)\_. A customer identifier, indicating who this instance of a resource is for | `string` | `null` | no |
| <a name="input_user"></a> [user](#input\_user) | Opsgenie User configuration | `map` | `{}` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_alert_policy_filter"></a> [alert\_policy\_filter](#output\_alert\_policy\_filter) | Filters of the Opsgenie Alert Policy |
| <a name="output_alert_policy_id"></a> [alert\_policy\_id](#output\_alert\_policy\_id) | The ID of the Opsgenie Alert Policy |
| <a name="output_alert_policy_name"></a> [alert\_policy\_name](#output\_alert\_policy\_name) | Name of the Opsgenie Alert Policy |
| <a name="output_alert_policy_priority"></a> [alert\_policy\_priority](#output\_alert\_policy\_priority) | Priority of the Opsgenie Alert Policy |
| <a name="output_alert_policy_responders"></a> [alert\_policy\_responders](#output\_alert\_policy\_responders) | Responders of the Opsgenie Alert Policy. |
| <a name="output_alert_policy_tags"></a> [alert\_policy\_tags](#output\_alert\_policy\_tags) | Tags of the Opsgenie Alert Policy |
| <a name="output_api_integration_api_key"></a> [api\_integration\_api\_key](#output\_api\_integration\_api\_key) | API key of the created integration |
| <a name="output_api_integration_id"></a> [api\_integration\_id](#output\_api\_integration\_id) | The ID of the Opsgenie API Integration |
| <a name="output_api_integration_name"></a> [api\_integration\_name](#output\_api\_integration\_name) | The name of the Opsgenie API Integration |
| <a name="output_escalation_id"></a> [escalation\_id](#output\_escalation\_id) | The ID of the Opsgenie Escalation |
| <a name="output_escalation_name"></a> [escalation\_name](#output\_escalation\_name) | Name of the Opsgenie Escalation |
| <a name="output_integration_action_id"></a> [integration\_action\_id](#output\_integration\_action\_id) | The ID of the Opsgenie Integration Action |
| <a name="output_notification_policy_id"></a> [notification\_policy\_id](#output\_notification\_policy\_id) | The ID of the Opsgenie Notification Policy |
| <a name="output_notification_policy_name"></a> [notification\_policy\_name](#output\_notification\_policy\_name) | The name of the Opsgenie Notification Policy |
| <a name="output_service_id"></a> [service\_id](#output\_service\_id) | The ID of the Opsgenie Service |
| <a name="output_service_incident_rule_id"></a> [service\_incident\_rule\_id](#output\_service\_incident\_rule\_id) | The ID of the Opsgenie Service Incident Rule |
| <a name="output_service_name"></a> [service\_name](#output\_service\_name) | The name of the Opsgenie Service |
| <a name="output_team_id"></a> [team\_id](#output\_team\_id) | The ID of the Opsgenie Team |
| <a name="output_team_name"></a> [team\_name](#output\_team\_name) | The name of the Opsgenie Team |
| <a name="output_team_routing_rule_id"></a> [team\_routing\_rule\_id](#output\_team\_routing\_rule\_id) | The ID of the Opsgenie Team Routing Rule |
| <a name="output_team_routing_rule_name"></a> [team\_routing\_rule\_name](#output\_team\_routing\_rule\_name) | The name of the Opsgenie Team Routing Rule |
| <a name="output_user_id"></a> [user\_id](#output\_user\_id) | The ID of the Opsgenie User |
| <a name="output_user_name"></a> [user\_name](#output\_user\_name) | The name of the Opsgenie User |
<!-- markdownlint-restore -->



## Share the Love

Like this project? Please give it a ★ on [our GitHub](https://github.com/cloudposse/terraform-opsgenie-incident-management)! (it helps us **a lot**)

Are you using this project or any of our other projects? Consider [leaving a testimonial][testimonial]. =)



## Related Projects

Check out these related projects.

- [terraform-datadog-monitor](https://github.com/cloudposse/terraform-datadog-monitor) - Terraform module to provision Standard System Monitors (cpu, memory, swap, io, etc) in Datadog


## References

For additional context, refer to some of these links.

- [Opsgenie API Overview](https://docs.opsgenie.com/docs/api-overview) - Opsgenie APIs give you interconnectivity to process your requests and access data. View our individual documentation for our APIs to see the methods used to process relevant requests. Action-specific instructions are included to help you complete requests, along with sample requests and responses for added guidance. Additionally, view our Rate Limiting section for specific details and configurations.
- [Terraform Registry Opsgenie Provider documentation](https://registry.terraform.io/providers/opsgenie/opsgenie/latest/docs) - The Opsgenie provider is used to interact with the many resources supported by Opsgenie. The provider needs to be configured with the proper credentials before it can be used.
- [Github Terraform OpsGenie provider repository](https://github.com/opsgenie/terraform-provider-opsgenie/) - The Opsgenie provider is used to interact with the many resources supported by Opsgenie. The provider needs to be configured with the proper credentials before it can be used.


## Help

**Got a question?** We got answers.

File a GitHub [issue](https://github.com/cloudposse/terraform-opsgenie-incident-management/issues), send us an [email][email] or join our [Slack Community][slack].

[![README Commercial Support][readme_commercial_support_img]][readme_commercial_support_link]

## DevOps Accelerator for Startups


We are a [**DevOps Accelerator**][commercial_support]. We'll help you build your cloud infrastructure from the ground up so you can own it. Then we'll show you how to operate it and stick around for as long as you need us.

[![Learn More](https://img.shields.io/badge/learn%20more-success.svg?style=for-the-badge)][commercial_support]

Work directly with our team of DevOps experts via email, slack, and video conferencing.

We deliver 10x the value for a fraction of the cost of a full-time engineer. Our track record is not even funny. If you want things done right and you need it done FAST, then we're your best bet.

- **Reference Architecture.** You'll get everything you need from the ground up built using 100% infrastructure as code.
- **Release Engineering.** You'll have end-to-end CI/CD with unlimited staging environments.
- **Site Reliability Engineering.** You'll have total visibility into your apps and microservices.
- **Security Baseline.** You'll have built-in governance with accountability and audit logs for all changes.
- **GitOps.** You'll be able to operate your infrastructure via Pull Requests.
- **Training.** You'll receive hands-on training so your team can operate what we build.
- **Questions.** You'll have a direct line of communication between our teams via a Shared Slack channel.
- **Troubleshooting.** You'll get help to triage when things aren't working.
- **Code Reviews.** You'll receive constructive feedback on Pull Requests.
- **Bug Fixes.** We'll rapidly work with you to fix any bugs in our projects.

## Slack Community

Join our [Open Source Community][slack] on Slack. It's **FREE** for everyone! Our "SweetOps" community is where you get to talk with others who share a similar vision for how to rollout and manage infrastructure. This is the best place to talk shop, ask questions, solicit feedback, and work together as a community to build totally *sweet* infrastructure.

## Discourse Forums

Participate in our [Discourse Forums][discourse]. Here you'll find answers to commonly asked questions. Most questions will be related to the enormous number of projects we support on our GitHub. Come here to collaborate on answers, find solutions, and get ideas about the products and services we value. It only takes a minute to get started! Just sign in with SSO using your GitHub account.

## Newsletter

Sign up for [our newsletter][newsletter] that covers everything on our technology radar.  Receive updates on what we're up to on GitHub as well as awesome new projects we discover.

## Office Hours

[Join us every Wednesday via Zoom][office_hours] for our weekly "Lunch & Learn" sessions. It's **FREE** for everyone!

[![zoom](https://img.cloudposse.com/fit-in/200x200/https://cloudposse.com/wp-content/uploads/2019/08/Powered-by-Zoom.png")][office_hours]

## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/cloudposse/terraform-opsgenie-incident-management/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing this project or [help out](https://cpco.io/help-out) with our other projects, we would love to hear from you! Shoot us an [email][email].

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull Request** so that we can review your changes

**NOTE:** Be sure to merge the latest changes from "upstream" before making a pull request!



## Copyrights

Copyright © 2021-2022 [Cloud Posse, LLC](https://cloudposse.com)





## License

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

See [LICENSE](LICENSE) for full details.

```text
Licensed to the Apache Software Foundation (ASF) under one
or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.  The ASF licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
```









## Trademarks

All other trademarks referenced herein are the property of their respective owners.

## About

This project is maintained and funded by [Cloud Posse, LLC][website]. Like it? Please let us know by [leaving a testimonial][testimonial]!

[![Cloud Posse][logo]][website]

We're a [DevOps Professional Services][hire] company based in Los Angeles, CA. We ❤️  [Open Source Software][we_love_open_source].

We offer [paid support][commercial_support] on all of our projects.

Check out [our other projects][github], [follow us on twitter][twitter], [apply for a job][jobs], or [hire us][hire] to help with your cloud strategy and implementation.



### Contributors

<!-- markdownlint-disable -->
|  [![Marcin Brański][3h4x_avatar]][3h4x_homepage]<br/>[Marcin Brański][3h4x_homepage] | [![Erik Osterman][osterman_avatar]][osterman_homepage]<br/>[Erik Osterman][osterman_homepage] | [![Andriy Knysh][aknysh_avatar]][aknysh_homepage]<br/>[Andriy Knysh][aknysh_homepage] | [![Igor Rodionov][goruha_avatar]][goruha_homepage]<br/>[Igor Rodionov][goruha_homepage] | [![Yonatan Koren][korenyoni_avatar]][korenyoni_homepage]<br/>[Yonatan Koren][korenyoni_homepage] | [![Benjamin Smith][benbentwo_avatar]][benbentwo_homepage]<br/>[Benjamin Smith][benbentwo_homepage] |
|---|---|---|---|---|---|
<!-- markdownlint-restore -->

  [3h4x_homepage]: https://github.com/3h4x
  [3h4x_avatar]: https://img.cloudposse.com/150x150/https://github.com/3h4x.png
  [osterman_homepage]: https://github.com/osterman
  [osterman_avatar]: https://img.cloudposse.com/150x150/https://github.com/osterman.png
  [aknysh_homepage]: https://github.com/aknysh
  [aknysh_avatar]: https://img.cloudposse.com/150x150/https://github.com/aknysh.png
  [goruha_homepage]: https://github.com/goruha
  [goruha_avatar]: https://img.cloudposse.com/150x150/https://github.com/goruha.png
  [korenyoni_homepage]: https://github.com/korenyoni
  [korenyoni_avatar]: https://img.cloudposse.com/150x150/https://github.com/korenyoni.png
  [benbentwo_homepage]: https://github.com/benbentwo
  [benbentwo_avatar]: https://img.cloudposse.com/150x150/https://github.com/benbentwo.png

[![README Footer][readme_footer_img]][readme_footer_link]
[![Beacon][beacon]][website]

  [logo]: https://cloudposse.com/logo-300x69.svg
  [docs]: https://cpco.io/docs?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=docs
  [website]: https://cpco.io/homepage?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=website
  [github]: https://cpco.io/github?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=github
  [jobs]: https://cpco.io/jobs?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=jobs
  [hire]: https://cpco.io/hire?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=hire
  [slack]: https://cpco.io/slack?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=slack
  [linkedin]: https://cpco.io/linkedin?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=linkedin
  [twitter]: https://cpco.io/twitter?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=twitter
  [testimonial]: https://cpco.io/leave-testimonial?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=testimonial
  [office_hours]: https://cloudposse.com/office-hours?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=office_hours
  [newsletter]: https://cpco.io/newsletter?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=newsletter
  [discourse]: https://ask.sweetops.com/?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=discourse
  [email]: https://cpco.io/email?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=email
  [commercial_support]: https://cpco.io/commercial-support?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=commercial_support
  [we_love_open_source]: https://cpco.io/we-love-open-source?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=we_love_open_source
  [terraform_modules]: https://cpco.io/terraform-modules?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=terraform_modules
  [readme_header_img]: https://cloudposse.com/readme/header/img
  [readme_header_link]: https://cloudposse.com/readme/header/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=readme_header_link
  [readme_footer_img]: https://cloudposse.com/readme/footer/img
  [readme_footer_link]: https://cloudposse.com/readme/footer/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=readme_footer_link
  [readme_commercial_support_img]: https://cloudposse.com/readme/commercial-support/img
  [readme_commercial_support_link]: https://cloudposse.com/readme/commercial-support/link?utm_source=github&utm_medium=readme&utm_campaign=cloudposse/terraform-opsgenie-incident-management&utm_content=readme_commercial_support_link
  [share_twitter]: https://twitter.com/intent/tweet/?text=terraform-opsgenie-incident-management&url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_linkedin]: https://www.linkedin.com/shareArticle?mini=true&title=terraform-opsgenie-incident-management&url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_reddit]: https://reddit.com/submit/?url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_facebook]: https://facebook.com/sharer/sharer.php?u=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_googleplus]: https://plus.google.com/share?url=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [share_email]: mailto:?subject=terraform-opsgenie-incident-management&body=https://github.com/cloudposse/terraform-opsgenie-incident-management
  [beacon]: https://ga-beacon.cloudposse.com/UA-76589703-4/cloudposse/terraform-opsgenie-incident-management?pixel&cs=github&cm=readme&an=terraform-opsgenie-incident-management

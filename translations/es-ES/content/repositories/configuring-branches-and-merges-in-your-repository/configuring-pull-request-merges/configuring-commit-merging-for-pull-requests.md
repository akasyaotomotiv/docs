---
title: Configuring commit merging for pull requests
intro: 'You can enforce, allow, or disable merging with a merge commit for all pull request merges on {% data variables.product.product_location %} in your repository.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
shortTitle: Configure commit merging
---

{% data reusables.pull_requests.configure_pull_request_merges_intro %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
1. Under {% ifversion fpt or ghec or ghes > 3.5 or ghae-issue-6069 %}"Pull Requests"{% else %}"Merge button"{% endif %}, select **Allow merge commits**. Esto permite que los contribuyentes fusionen una solicitud de cambios con un historial completo de confirmaciones.{% ifversion default-merge-squash-commit-message %} ![Screenshot of Pull Request settings with allow merge commits checkbox emphasized](/assets/images/help/repository/allow-merge-commits.png){% endif %}{% ifversion ghes = 3.6 %} ![Screenshot of Pull Request settings with allow merge commits checkbox emphasized](/assets/images/help/repository/allow-merge-commits-no-dropdown.png){% endif %}
{% ifversion ghes < 3.6  %}
 ![allow_standard_merge_commits](/assets/images/help/repository/pr-merge-full-commits.png){% endif %}
{% ifversion default-merge-squash-commit-message %}
1. Optionally, under **Allow merge commits**, use the dropdown to choose the format of the commit message presented to contributors when merging. The default message includes the pull request number and title. For example, `Merge pull request #123 from patch-1`. You can also choose to use just the pull request title, or the pull request title and description. ![Screenshot of emphasized default commit message dropdown](/assets/images/help/repository/default-commit-message-dropdown.png)
{% endif %}

Si seleccionas más de un método de fusión, los colaboradores pueden elegir qué tipo de confirmación de fusión utilizar cuando fusionan una solicitud de cambios. {% data reusables.repositories.squash-and-rebase-linear-commit-history %}

## Leer más

- "[Acerca de las fusiones de solicitudes de extracción](/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges)"
- "[Fusionar una solicitud de extracción](/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request)"

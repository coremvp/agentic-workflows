# UI reference directory

Start with the application's approved UI and useful information. Inspect exact
examples and show relevant pictures for an unsettled direction; this index is
not a completed case study. Library names are conditional options, not claims
that they are installed. Preserve the host's framework, theme and permissions.

| Design problem | Reference | Useful decision and fit |
| --- | --- | --- |
| Navigation/workspaces | [shadcn Sidebar](https://ui.shadcn.com/docs/components/radix/sidebar) | Grouping, collapsed navigation and mobile behavior; adapt to existing primitives. |
| Forms/validation | [shadcn forms](https://ui.shadcn.com/docs/forms/react-hook-form), [Radix Dialog](https://www.radix-ui.com/primitives/docs/components/dialog) | Field hierarchy, feedback and focus; check the installed form/dialog owners and retain server validation. |
| Compact lists | [shadcn Item](https://ui.shadcn.com/docs/components/radix/item) | Title, secondary detail and next action without redundant panels; composition does not require adding Item. |
| Tables/filtering | [shadcn Data Table](https://ui.shadcn.com/docs/components/radix/data-table), [TanStack filtering](https://tanstack.com/table/latest/docs/framework/react/examples/filters) | Density, sorting/filter interaction and pagination; use the actual table/query owners before adopting another dependency. |
| Product/dashboard hierarchy | [Linear Projects](https://linear.app/docs/projects) | Compact properties, resources and updates; do not copy fields or imply absent data. |
| Time-series charts | [shadcn area charts](https://ui.shadcn.com/charts/area) | Honest units, comparisons, axes and tooltip; a useful source and compatible installed chart library are prerequisites. |
| Empty states/onboarding | [shadcn Empty](https://ui.shadcn.com/docs/components/radix/empty), [signup blocks](https://ui.shadcn.com/blocks/signup) | One useful first action; preserve existing authentication and redirects, not a new funnel by default. |
| Landing/product demonstrations | [Magic UI Terminal](https://magicui.design/docs/components/terminal) | A truthful command/result relationship; distinguish illustration from execution and respect reduced motion. |

Add a source only for a distinct useful problem. Keep fit notes/links, not copied
third-party assets. Check current examples and APIs during the relevant task.

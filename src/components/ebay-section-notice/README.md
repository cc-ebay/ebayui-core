<h1 style='display: flex; justify-content: space-between; align-items: center;'>
    <span>
        ebay-section-notice
    </span>
    <span style='font-weight: normal; font-size: medium; margin-bottom: -15px;'>
        DS v1.0.0
    </span>
</h1>

The `<ebay-section-notice>` is a tag used to create a custom-designed notice element. The notice can be single or multi-line but each line should be wrapped inside a `<p>` tag.

This notice should be used at the top of various sections to display information needed.

## ebay-section-notice Usage

```marko
<ebay-section-notice a11y-text="Attention" status="attention">
    <p>Couldn't load all the items, please try again later.</p>
</ebay-section-notice>
```

```marko
<ebay-section-notice a11y-text="Attention" status="attention">
    <p>Couldn't load all the items, please try again later.</p>
    <@footer><ebay-fake-link>Try again</ebay-fake-link></@footer>
</ebay-section-notice>
```

## ebay-section-notice Sub-tags

| Tag         | Required | Description                             |
| ----------- | -------- | --------------------------------------- |
| `<@footer>` | No       | The footer content (for ebay-fake-link) |

## ebay-section-notice Attributes

| Name                    | Type   | Stateful | Required | Description                                                                                        |
| ----------------------- | ------ | -------- | -------- | -------------------------------------------------------------------------------------------------- |
| `status`                | String | No       | No       | "attention" "confirmation" "information". The default will render with grey background and no icon |
| `a11y-text`             | String | No       | Yes      | the description for the notice icon for a11y users.                                                |
| `a11y-role-description` | String | No       | Yes      | The roledescription to announce the component type for a11y users. Defaults to "Notice".           |
| `icon`                  | String | Yes      | No       | "default" (matches whatever is specified by the "status") or "none"                                |

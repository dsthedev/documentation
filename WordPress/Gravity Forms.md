# Gravity Forms

## New Form Guide

Before creating a form, it's important to run through the settings first.  Even if there will be complex conditional logic in them.  At the very least some foundations can be set, and notes for future changes can be recorded.

1. Form Settings
	1. Title and description should be short and succinct.
	2. Keep the device the form will be used on most here (mobile vs desktop)
	3. Form button's text should be relevant and short.  Logic is used to show/hide the button based on field value
	4. Save and continue should be used with caution, after a thorough needs analysis
	5. Restrictions for entry limit, scheduled availability, and user-only access
	6. I usually enable both honeypot and animated transitions in Form Options
		1. Unless a recaptcha is needed for extra security
2. Confirmations - Make sure the user knows the form has been submitted or saved.
3. .
	1. .

## Tips

### Merge Tags

* The label isn't necessary `{Field Label:17} > {:17}`
* [Modifiers](https://docs.gravityforms.com/merge-tags/#all-fields) are added *after* the ID `{:17:value}`
* It's possible to dynamically populate a field using merge tags with this [gist](https://gist.github.com/spivurno/7029518)

### Ready Classes

Here's all of the "CSS Ready Classes" in one simple list.

```plaintext
gf_left_half
gf_right_half
gf_left_third
gf_middle_third
gf_right_third
gf_list_2col
gf_list_3col
gf_list_4col
gf_list_5col
gf_list_inline
gf_list_height_25
gf_list_height_50
gf_list_height_75
gf_list_height_100
gf_list_height_125
gf_list_height_150
gf_scroll_text
gf_hide_ampm
gf_hide_charleft
```
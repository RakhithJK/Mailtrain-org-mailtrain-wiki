> This feature applies to Mailtrain v1.3+ which at the moment is available from a [development branch](https://github.com/andris9/mailtrain/tree/v1.3)

When setting up a new campaign you can either select a template or an URL as the message contents. If you choose an URL then every time a message is sent or a message is rendered in the browser (through *View this email in your browser* link), a POST request is made against that URL. Request body includes all merge tags related to this subscriber the messages is rendered for.

![](https://cldup.com/0aJnw3Pr8A.png)

Here's an example PHP script for responding to render requests at `http://example.com/newsletter.php`:

```php
<p>Hello <?= $_POST['FULL_NAME'] ?></p>

<p>This is a test message, <a href="https://google.com">visit Google</a></p>

<p>Bye!</p>

<hr />

<p>
    <a href="<?= $_POST['LINK_UNSUBSCRIBE'] ?>">Unsubscribe</a>
    |
    <a href="<?= $_POST['LINK_PREFERENCES'] ?>">Preferences</a>
    |
    <a href="<?= $_POST['LINK_BROWSER'] ?>">View this message in a browser</a>
</p>
```
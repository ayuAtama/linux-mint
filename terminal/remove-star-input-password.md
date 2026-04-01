To remove the star when input password, run the following command:

```bash
echo 'Defaults !pwfeedback' | sudo tee /etc/sudoers.d/9_no_pwfeedback
```

To bring it back run the following command:

```bash
sudo rm /etc/sudoers.d/9_no_pwfeedback
```

# action-ipadown

Download old versions of app using Github Actions, without computers!

**Warning: NOT supporting 2FA accounts currently**

## Use Cases

- Buy & Download App
- Download Old Versions of App
- Query Version History of App
- Lookup app information based on bundleID or appID

## Usage

1. Fork this repo
2. Enable Actions in forked repo
  - Click Actions in toolbar
  - Click `I understand my workflows, go ahead and enable them`
      ![image](https://user-images.githubusercontent.com/5344431/167505409-ef077008-2450-4e2d-9d43-2067244ac931.png)
3. Run Action
  - Click `IPA Down` in left list:
      ![image](https://user-images.githubusercontent.com/5344431/167505630-1a741d9c-69de-470c-978e-1b8944dcfd3b.png)
  - Click `Run workflow` at right:
      ![image](https://user-images.githubusercontent.com/5344431/167505748-52e0bba9-b9ec-44e1-9370-4452d3c3c66b.png)
  - Enter Apple ID, Password, Operation and corresponding parameters (like bundleID)
  - Click `Run workflow`
  - Find output files in Actions artifact or Release
      ![image](https://user-images.githubusercontent.com/5344431/167506938-c3e3529c-ee91-4661-a251-a12a2d0576cb.png)
  - If the actions fails at `Setup iTunes Header Service`, please retry 1~2 times before submitting issue

## Operations

There are currently five operations: lookup, historyver, download, historyver_id, download_id

- lookup: query information of app based on bundleID
- historyver: query history appVerID by bundleID (with historyver_id querys by appID)
- download: download IPA by bundleID (download_id uses appID) & appVerID (optional, defaults to newest version)

To use these operations, enter your app informations like this:
- Using Bundle ID:
  ![image](https://user-images.githubusercontent.com/5344431/167506427-1503417c-112f-4c45-b82b-7887f05b0dac.png)
- Using appID:
  ![image](https://user-images.githubusercontent.com/5344431/167506645-d29db175-ab38-45d3-b224-6cc94131e61d.png)
- Also giving appVerID:
  ![image](https://user-images.githubusercontent.com/5344431/167506870-8dcaa565-3bd1-424e-a9d2-eed00bd4cffb.png)

## Credits

- ipatool-py: https://github.com/NyaMisty/ipatool-py
- actions-iTunes-header: https://github.com/NyaMisty/actions-iTunes-header

# Kibana Sankey Diagram Plugin

This is a sankey diagram visType plugin for Kibana 5.5.0+.

This plugin was developped from <https://github.com/elastic/kibana/pull/4832>.

Here is an example:

![Sankey](Capture1.PNG)

# Install

```
git clone https://github.com/LeonAgmonNacht/kbn_sankey_vis
cd kbn_sankey_vis
npm install d3-sankey-plugin
cp -R kbn_sankey_vis KIBANA_FOLDER_PATH/src/core_plugins
```
** Note that if your kibana version is not 5.5.0, you need to change it in package.json

** Note that in NTFS file systems, file paths that exceed 260 characters will fail with cp, you have to use ROBOCOPY:

```
robocopy /S kbn_sankey_vis KIBANA_FOLDER_PATH/installedPlugins/kbn_sankey_vis
```

** Also note that if npm run build fails, with a rsync.js error, it is likelly that you don't have RSYNC.EXE installed
in your system, and also that you don't have it on your PATH environment variable.

Install it from https://www.itefix.net/cwrsync and run:

```
set PATH=%PATH%;{rsync installation directory}\bin
```

# Uninstall

```
rm kbn_sankey_vis in src/core_plugins
rm kibana.bundle.js in optimize/bundles
re-run Kibana
```

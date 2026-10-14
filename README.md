# JEBAL Lake House

Editable architectural study, render gallery and browser development workspace.

**[Open browser editor](https://github.dev/ammr006/JEBAL)** · **[Open a Codespace](https://github.com/codespaces/new?hide_repo_select=true&repo=1419405621)**

## Start here

- [Current design status](docs/CURRENT_STATUS.md)
- [Editable current model](output/JEBAL_Stage_Kitchen_v23/JEBAL_Stage_Kitchen_v23.blend)
- [Stage and kitchen dimensions](output/JEBAL_Stage_Kitchen_v23/README.md)
- [Geometry checks](output/JEBAL_Stage_Kitchen_v23/evidence/layout_checks.json)
- [Visual gallery](docs/GALLERY.md)
- [Files and SHA-256 hashes](PUBLIC_FILE_MANIFEST.json)

![Current native model](output/JEBAL_Stage_Kitchen_v23/renders/01_MASTER_AERIAL.png)

## Work in the browser

Use **github.dev** to edit scripts, documentation and configuration; commit changes to save them to GitHub. It does not run Python or Blender.

For a terminal and preview server, select **Code → Codespaces → Create codespace on main**. The included devcontainer installs the Python presentation dependencies. Codespaces usage is subject to your GitHub allowance.

```sh
python -m http.server 8000
```

Open the forwarded port 8000 to view the image gallery. Edit `index.html`, design notes or scripts in the same browser workspace.

For geometry work, use Blender 5.x in an environment with Blender installed (validated with Blender 5.2):

```sh
blender --background --disable-autoexec --python tools/validate_scene.py
blender --background --disable-autoexec --python tools/render_scene.py -- --list
blender --background --disable-autoexec --python tools/render_scene.py -- --camera 01_MASTER_AERIAL --preview
```

The browser editor does not provide an interactive Blender viewport. A Codespace can run headless Blender after Blender is installed; the devcontainer does not bundle Blender.

To rebuild the design presentation:

```sh
python -m pip install -r requirements.txt
python output/JEBAL_Rock_Finish_v25/build_presentation.py
```

## Project scope

The current coordinated geometry is **v23**. **v25** changes the presentation's conceptual rock finish, not the native model. The wave canopy images are archived alternatives. Furniture boards are design alternatives, not a confirmed supplier order or a change to the saved model.

This is an active working subset, **not the multi-gigabyte archival backup or a native Codex chat migration**. Private chat transcripts, commercial partnership discussions, credentials, raw venue footage, downloaded third-party asset libraries, caches and backup ZIP files are excluded from this public repository. Existing backups remain separate.

Design review material; dimensions and structural, fire/egress and kitchen engineering assumptions require professional verification before construction. No open-source license is granted by this upload.

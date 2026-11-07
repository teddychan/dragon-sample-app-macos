# Changelog

Changes in each version of Dragon Sample App, newest first. Each entry is also that version's tag
message and the notes of its GitHub Release.

Versions before 1.4.2 were released from the DragonKit repository. Tags v1.4.1 and v1.4.7 exist
but never became a release.

## [1.6.0] - 2026-11-07

Dragon Sample App looks and works the same as 1.5.0. This version moves it to DragonKit 4.4.0.

### Internal

- Updated to DragonKit 4.4.0, the shared framework behind the menu, Settings, About, What's New
  and software updates. DragonKit now removes the app's settings during Uninstall on its own, so
  the app no longer lists them. Uninstall removes the same settings as before. The About screen
  shows the new DragonKit version.

## [1.5.0] - 2026-11-03

Dragon Sample App now comes in Russian, and on macOS 27 its menu shows its icons again.

### Added

- Russian. Choose Русский under Language in Settings > General, and the menu, Settings, About and
  What's New all switch to it.

### Fixed

- On macOS 27 the About, Check for Updates, Settings and Quit items in the menu bar menu had no
  icons. The icons are back. Older versions of macOS look the same as before.

### Changed

- Updated to DragonKit 4.3.0, the shared framework behind the menu, Settings, About, What's New
  and software updates. The icon fix above comes from it.

## [1.4.9] - 2026-08-20

A safety fix in Uninstall, from DragonKit, the shared framework Dragon Sample App is built on. The
menu bar icon and the sample settings are unchanged.

### Fixed

- Uninstall now stops if it finds more than one copy of Dragon Sample App on your Mac. Your
  settings, login item and support files belong to the app's identity, not to where a copy sits,
  so every copy shares them, and uninstalling a spare copy could remove the settings of the copy
  you use. Uninstall now removes nothing and lists where the copies are, so you can move the ones
  you don't want to the Trash and try again. With one copy, nothing changes.

### Changed

- Updated to DragonKit 4.1.1, the shared framework behind Settings, About, What's New and software
  updates. The fix above comes from it, and none of those panes look or work differently.

## [1.4.8] - 2026-08-18

Nothing in the app changed. This release tested the full publishing path.

### Changed

- Releases now go through pull requests from start to finish: prepared, merged, tagged and
  published without writing to any branch directly.

## [1.4.6] - 2026-08-18

A maintenance release: Dragon Sample App now builds against DragonKit 4.1.0.

### Changed

- Raised the DragonKit requirement to 4.1.0, its newest release at the time.

## [1.4.5] - 2026-08-11

The app now carries a copyright notice, the same one About shows.

### Fixed

- Finder's Get Info window now shows Dragon Sample App's copyright notice, which was missing.

## [1.4.4] - 2026-08-11

Two fixes in the About pane.

### Fixed

- About credited Sparkle under the MIT license but had no way to read its license notice. A new
  Open-source licenses row opens the notices at
  https://www.dragonapp.com/dragon-sample-app/licenses/.
- The support link sent bug reports to DragonKit's issue tracker, left over from when the app lived
  inside DragonKit. It now opens this app's own repository.

## [1.4.3] - 2026-08-11

A maintenance release on DragonKit 3.4.0.

### Changed

- Updated to DragonKit 3.4.0. About's "Built with" row shows the new version.

## [1.4.2] - 2026-08-10

The first release from Dragon Sample App's own repository. Nothing you use in the app changed.

### Changed

- Dragon Sample App now has its own repository, version tags and update feed, apart from
  DragonKit, so the app and the framework each keep their own version numbers.
- Update checks read the app's own feed. Copies of 1.4.0 still check the old feed in the DragonKit
  repository and won't be offered this update: install 1.4.2 or later with Homebrew or from the
  GitHub Release.

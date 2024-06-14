# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: DachiNatenadze
          template: classic
          base: header, activity, community, repositories, metadata
          base_indepth: yes
          config_display: large
          config_timezone: Asia/Tbilisi
          plugin_calendar: yes
          plugin_calendar_limit: 2024
          plugin_gists: yes
          plugin_introduction: yes
          plugin_introduction_title: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_analysis_timeout_repositories: 7.5
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_limit: 8
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used
          plugin_languages_threshold: 0%
          plugin_music: yes
          plugin_music_limit: 4
          plugin_music_mode: playlist
          plugin_music_played_at: yes
          plugin_music_playlist: https://www.youtube.com/watch?v=kLAUo2kDgHo&list=RDkLAUo2kDgHo&start_radio=1
          plugin_music_provider: youtube
          plugin_music_time_range: short
          plugin_music_top_type: tracks
          plugin_music_user: .user.login
          plugin_steam: yes
          plugin_steam_achievements_limit: 2
          plugin_steam_games_limit: 1
          plugin_steam_playtime_threshold: 2
          plugin_steam_recent_games_limit: 1
          plugin_steam_sections: player, most-played, recently-played
          plugin_steam_user: Steamcommunity.com/profiles/76561199548290136/

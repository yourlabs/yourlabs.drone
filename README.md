yourlabs.timer
==============

Example usage with bigsudo (for one-shot):

    bigsudo yourlabs.timer name=your-backup cmd=/your/backup.sh oncalendar='*-*-* 00:00:00 Europe/Paris'

Example usage in task:

    - name: Setup backup cron
      include_role: name=yourlabs.timer
      vars:
        name: '{{ project_instance }}-backup'
        cmd: '{{ home }}/sh.yml backup'
        chdir: '{{ home }}'
        oncalendar: '*-*-* 23:00:00'

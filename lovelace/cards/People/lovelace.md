![image](https://user-images.githubusercontent.com/63735432/141701685-c8fa79bb-9693-4324-9801-71ab41172d07.png)

```
# Manual card
type: custom:stack-in-card
title: ''
mode: vertical
cards:
  - type: picture-elements
    elements:
      - type: conditional
        style:
          display: inline
          position: absolute
          transform: translate(0%, 0%)
          width: 48%
          top: 4%
          left: 2%
          bottom: 4%
          font-size: clamp(.85rem, 1vw, 1rem)
          white-space: nowrap
          overflow: hidden
          text-overflow: ellipsis
          padding-right: 2%
        conditions:
          - entity: person.person1
            state_not: '0'
        elements:
          - type: image
            entity: person.person1
            title: person1
            image: /local/ha.png
            style:
              transform: translate(0%, 0%)
              width: 40%
              border-radius: 50%
          - type: conditional
            conditions:
              - entity: person.person1
                state_not: '0'
            elements:
              - type: state-icon
                icon: mdi:car
                entity: sensor.person1_time_to_home
                style:
                  transform: translate(0%, 0%)
                  left: 40%
                  position: realitive
              - type: state-label
                prefix: ''
                entity: sensor.person1_time_to_home
                style:
                  transform: translate(0%, 0%)
                  left: 51%
                  top: 1.5%
              - type: state-icon
                icon: mdi:speedometer
                entity: sensor.person1s_speed_mph
                style:
                  transform: translate(0%, 0%)
                  left: 40%
                  top: 10%
              - type: state-label
                suffix: ''
                entity: sensor.person1s_speed_mph
                style:
                  transform: translate(0%, 0%)
                  left: 51%
                  top: 11.5%
          - type: conditional
            conditions:
              - entity: binary_sensor.workday
                state_not: 'off'
            elements:
              - type: state-icon
                icon: mdi:office-building-marker-outline
                entity: sensor.person1_time_to_work
                style:
                  transform: translate(0%, 0%)
                  left: 40%
                  top: 20%
              - type: state-label
                prefix: ''
                entity: sensor.person1_time_to_work
                style:
                  transform: translate(0%, 0%)
                  left: 51%
                  top: 21.5%
          - type: state-label
            entity: person.person1
            prefix: 'person1: '
            style:
              transform: translate(0%, 0%)
              top: 35%
              font-weight: bold
              font-size: clamp(.85rem, 1.1rem, 1.5rem)
          - type: state-label
            entity: input_text.person1s_location
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 42%
              font-size: .8rem
          - type: state-icon
            entity: sensor.person1s_phone_battery_level
            style:
              transform: translate(0%, 0%)
              top: 52%
          - type: state-label
            entity: sensor.person1s_phone_battery_level
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 54%
              left: 11%
          - type: state-label
            entity: sensor.person1s_phone_battery_state
            prefix: ' - '
            style:
              transform: translate(0%, 0%)
              top: 54%
              left: 26.5%
          - type: state-icon
            entity: binary_sensor.person1s_phone_mobile_data
            style:
              transform: translate(0%, 0%)
              top: 62%
          - type: state-label
            entity: binary_sensor.person1s_phone_mobile_data
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 64%
              left: 11%
          - type: state-icon
            entity: sensor.person1s_phone_wifi_connection
            style:
              transform: translate(0%, 0%)
              top: 62%
              left: 25%
          - type: state-label
            entity: sensor.person1s_phone_wifi_connection
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 64%
              left: 36%
          - type: state-icon
            entity: binary_sensor.person1s_phone_bluetooth_state
            style:
              transform: translate(0%, 0%)
              top: 72%
          - type: state-label
            entity: binary_sensor.person1s_phone_bluetooth_state
            prefix: 'Bluetooth: '
            style:
              transform: translate(0%, 0%)
              top: 74%
              left: 11%
          - type: state-icon
            entity: sensor.person1s_phone_do_not_disturb_sensor
            style:
              transform: translate(0%, 0%)
              top: 82%
          - type: state-label
            entity: sensor.person1s_phone_do_not_disturb_sensor
            prefix: 'Do not distrub: '
            style:
              transform: translate(0%, 0%)
              top: 84%
              left: 11%
      - type: conditional
        style:
          display: inline
          position: absolute
          transform: translate(0%, 0%)
          width: 48%
          top: 4%
          left: 50%
          bottom: 4%
          font-size: clamp(.85rem, 1vw, 1rem)
          white-space: nowrap
          overflow: hidden
          text-overflow: ellipsis
          padding-right: 2%
        conditions:
          - entity: person.person2
            state_not: '0'
        elements:
          - type: image
            entity: person.person2
            title: person2
            image: /local/ha.png
            style:
              transform: translate(0%, 0%)
              width: 40%
              border-radius: 50%
          - type: state-label
            entity: person.person2
            prefix: 'person2: '
            style:
              transform: translate(0%, 0%)
              top: 35%
              font-weight: bold
              font-size: clamp(.85rem, 1.1rem, 1.5rem)
          - type: state-label
            entity: input_text.person2s_location
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 42%
              font-size: .8rem
          - type: state-icon
            entity: sensor.person2s_phone_battery_level
            style:
              transform: translate(0%, 0%)
              top: 52%
          - type: state-label
            entity: sensor.person2s_phone_battery_level
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 54%
              left: 11%
          - type: state-label
            entity: sensor.person2s_phone_battery_state
            prefix: ' - '
            style:
              transform: translate(0%, 0%)
              top: 54%
              left: 26.5%
          - type: state-icon
            entity: binary_sensor.person2s_phone_mobile_data
            style:
              transform: translate(0%, 0%)
              top: 62%
          - type: state-label
            entity: binary_sensor.person2s_phone_mobile_data
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 64%
              left: 11%
          - type: state-icon
            entity: sensor.person2s_phone_wifi_connection
            style:
              transform: translate(0%, 0%)
              top: 62%
              left: 25%
          - type: state-label
            entity: sensor.person2s_phone_wifi_connection
            prefix: ''
            style:
              transform: translate(0%, 0%)
              top: 64%
              left: 36%
          - type: state-icon
            entity: binary_sensor.person2s_phone_bluetooth_state
            style:
              transform: translate(0%, 0%)
              top: 72%
          - type: state-label
            entity: binary_sensor.person2s_phone_bluetooth_state
            prefix: 'Bluetooth: '
            style:
              transform: translate(0%, 0%)
              top: 74%
              left: 11%
          - type: state-icon
            entity: sensor.person2s_phone_do_not_disturb_sensor
            style:
              transform: translate(0%, 0%)
              top: 82%
          - type: state-label
            entity: sensor.person2s_phone_do_not_disturb_sensor
            prefix: 'Do not distrub: '
            style:
              transform: translate(0%, 0%)
              top: 84%
              left: 11%
    image: /local/smallcard.png
    aspect_ratio: 55.5%
  - type: grid
    cards:
      - type: custom:button-card
        color: auto
        aspect_ratio: 1/.12
        name: Find person1's Phone
        styles:
          card:
            - left: '-15%'
            - top: '-25%'
        tap_action:
          action: call-service
          service: script.find_person1s_phone
      - type: custom:button-card
        color: auto
        aspect_ratio: 1/.12
        name: Find person2's Phone
        styles:
          card:
            - top: '-25%'
            - left: '-15%'
        tap_action:
          action: call-service
          service: script.find_person2s_phone
    columns: 2
    square: false

```

```
Usage: t frw audcap [command]
    open         opens audio capture
    select       select which audio capture mods(0|1) , optional pattern(0xabcd)
    start        starts audio capture
    stop         stops audio capture
    suspend      suspends the audio capture
    resume       resumes the audio capture
    attach       attach liveplay to capture for test
    detach       detach liveplay from capture for test
    debug        silent|api|cap|enc|capp2p|encp2p|info
    sc <ctrl parm> <option>
==============================================
    ctrl params          options
    -----------          -------
    spl<spl measurement>  enable
    bl <bl algo>          disable
    fin <file input>      report
    fout <file output>
    cfout <capture file out>
```

```
Usage: t frw audproc [command]
    open         opens audio process
    vr           set VR (on=1|off=0)
    vr_language  set VR language(0-10)
    vr_state     set VR state(LPM=0|Main=1|Rec=2)
    vr_source    set VR source(mic=0|BT=1|none=-1)
    calib        set mic calib (enable=1|disable=0)
    awe_mode     set AWE modes(dynamics=0|FixedGain=1|wind=2|stereo=3|auto=4)
    mic_src      set mic source(int=0|ext=1)
    bt_wt        set BT audio weight(weight=0-100)
    protune      set protune(on=1|off=0)
    protune_mode set protune modes(raw=0|wind=1|full=2)
    mic_raw      set mic raw (enable=1|disable=0)
    enable_awe   set enable AWE flag(0=skip|1=enable)
    vr_mem       test VR memory pool(malloc=1|free=0)
    awe_prof     take a profiling snapshot of AWE
    start        starts audio process
    stop         stops audio process
    suspend      suspends the audio process
    resume       resumes the audio process
    attach       attach liveplay to process for test
    detach       detach liveplay from process for test
```

```
Usage: t frw audsink [command]
         open           open audio output task
         close          close audio output task
         switch <port>  select I2S port <0|1>
         skip_beep <flag>  skip beep <0=false|1=true>
         select <id>    select the audio output <1=BUILTIN, 2=LINE_OUT, 3=HP(EDB), 4=HDMI, 5=HEROBUS
         start          starts audio sink
         stop           stops audio sink
         get_volume     get volume levels on audio sink and beep
         pb_volume <level> set playback volume(0-100)
         beep_volume <level> set beep volume(0-100)
         beep <1-10>    start a beep with index
         playfile <filename>    play a PCM file, such as C:\test.pcm
         setctrl <type> set the type of audio sink
         getctrl        show the selected audio sink type
         debug          silent|api|out|dec|outp2p|decp2p|info
         fio            <in|out><1(enable)|0(disable)>
```

```
Usage: t frw audsrc [command]
         open        opens the audio source
         start       starts the opened source module
         stop        stops the opened module
         select <id> selects the audio source <1=ONBOARD, 2=LINEIN, 3=GP_MIC_BT, 4=HEADSET(EDB),5=HEROBUS
```

```
Usage: t frw datacap [command]
         start  starts forwarding data
         stop   stops forwarding data
         add   add data
```

```
Usage: t frw disp low_latency [enable|disable]
```

```
Usage: t frw disp hdmi [enable|disable]
```

```
Usage: t frw pb [command]
         rotate
         dma_rotate
         show
         clear
         show
         pattern <x> <y> <width> <height> <color>
```

```
Usage: t frw windows [Command] [Parameters]
     Command        Parameters                     Description
     info                                          Display windows information
     orientation                                   Display orientation information
     transform      WxH@(x,y) winIdIn winIdOut     Transform rectangle from a window to another
```

```
Usage: t frw iq [Command]  [Parameters]
     Command        Parameters     Description
      disp          on/off         Enable Traces
      load                         Load All IQ Tables
      still[_mode]  mode           IQ Table Still Mode Index
      scene[_no]    number         IQ Table Scene Number Index
      stat[istics]                 Display IQ settings/statistics
      show                         Display IQ headers
      ob[mode]      iq/auto        Optical Black Mode
      sgde[_scaler] <0-4>          SGDE Kernel (0=Weakest...4=Strongest)
```

```
Usage: t frw cal [Command]  [Parameters]
   Command         Parameters            Description
      osd          [lcd/hdmi/on/off]     Enable/Disable OSD Calibration Display
      raw          [12/16/off]           Raw12/Raw16/Disable Raw Bayer Capture
      tsk_dsp      start/stop/clean
      tsk_dsp      out 0
      tsk_dsp      out 1 [filename]
```

```
Usage: t frw fshd [Command]  [Parameters]
     Command         Parameters            Description
      sho[w]                               Show FSHD table summary
      disp           on/off                Display FSHD diagnostic traces
      load                                 Load FSHD Tables
      comp[ensation] on/off  [dmsc_id]     Enable Frame/Lens Shading Compensation
      col[ortemp]    [4000-6000] [dmsc_id] Set FSHD Color Temperature in Kelvin
      rat[io]        [1-999]  [dmsc_id]    Set FSHD Corner Ratio Value
      fl[ip]         0/1  [dmsc_id]        Enable(1)/Disable(0) FSHD Table Flip
      stat[istics]   [dmsc_id]             Display current FSHD settings
      strength       [0 - 200]%%            Change FSHD table with new strength
      maskRB         on/off                Mask R & B Channels in FSHD Tables
```

```
Usage: t frw badpix [Command]  [Parameters]
   Command         Parameters            Description
   sho[w]                               Show Bad Pixel summary
   stat[istics]                         Display Bad Pixel Statistics
   load                                 Load Bad Pixel Table
   comp[ensation]  on/off  [sen_id]     Enable Bad Pixel Compensation
   force           on/off x y           Force Bad Pixel Parameters
   dis[play]       [bp_index] [max]     Display Bad Pixel table
```

```
Usage: t frw 3a [Command] [Parameters]
    Command       Parameters          Description
     info                              Display 3a information
     dispiq        on/off              Display 3a->IQ Param Changes
     disp[xxx]     on/off              [xxx=ae/stillae/awb/stillawb/lib/] traces
     disposd       on/off              Display 3a on OSD
     win[dow]                          Display window setting
     stat[istics]  [index]             Display 3A stats
     bayer         gp/sni              Select Bayer Scaler
     aflip         on/off              ?
     ae            auto/manual
     shutter       <float>             GPCC-AE   Set/Get shutter time in seconds
     isomin        value               GPCC-AE   Set iso min value, 0=auto
     isomax        value               GPCC-AE   Set iso max value, 0=auto
     iso           value               GPCC-AE   Get current iso value
     getevc                            Display EV Correction Value
     setevc        ev_corr [sensor_id] Set EV Correction Value
            ev_corr - 0, +/-32768, +/-65536  = 0,0, +/-1/2, +/-1.0
     submodeinfo                       GPCC-AE   Display current mode/submode info needed for AE configuration
     gptest                            GPCC-???
     awb           auto/kelvin         GPCC-AWB  Set protune WB (protune values only)
     forcect                           GPCC-AWB  Force the color temperature sent to the IQ bin (any value)
     forcewbgain                       GPCC-AWB  Force HW WB scales
     forcecm       9 values            GPCC-AWB  Force HW 3x3 color matrix (512=1.0)
     mccdef        on/off              GPCC-AWB  enable/disable color matrix
     forcebprgb    r g b y             GPCC-GTM  Force HW RGB blackpoint
     histomode     value               GPCC-GTM  Force R2Y TCHS RGB histograms slicing
     histosamp     x y                 GPCC-GTM  Force R2Y TCHS histograms subsampling
     gamma                             GPCC-GTM  Print gamma curve
     senreg                            GPCC-Debug Print SEN unit registers
     sroreg                            GPCC-Debug Print SRO unit registers
     obtreg                            GPCC-Debug Print SEN OBT optical black correction registers
     fshdl0 reg                        GPCC-Debug Print SRO FSHDL0 color lens shading correction registers
     fshdreg                           GPCC-Debug Print B2B FSHD lens shading registers
     wbgainreg                         GPCC-Debug Print B2R WB gain registers
     ccreg                             GPCC-Debug Print R2Y CC0 color matrix application registers
     gtmreg                            GPCC-Debug Print R2Y GTM-related registers
     aeawbreg                          GPCC-Debug Print STAT AEAWB statistics registers
```

```
Usage: t frw sni [Command] [Parameters]
    Command        Parameters    Description
     disp          on/off        Display 3a diagnostic traces
     stat                        Display SNI 3a stats
     ae                          auto/manual
     awb                         auto/manual
```

t frw gpcc

```
Usage: t frw imgcap [command]
    fd         <enable/disable>
    3dnr       <enable/disable>
    ltm        <enable/disable>
    gp_ltm     <enable/disable>
    mfnr       <enable/disable>
    dzoom      <enable/disable>
               test_dzoom_repeat repeat_no<1-100> interval_in_ms<0-1000>
               dzoom_eff_val <0-256>
    ae_info    <enable/disable>
    clean_raw  <enable/disable>
    eis        <enable/disable>
               info
               algo <fotonation/hypersmooth/lowlatency/stub/disable/unset>
               gp ...
               first_sample_time
               strength min_val(0.0 to 1.0) max_val(0.0 to 1.0)
               strengthlut idx (makes lut idx the current lut)
               strengthlut idx val0 val1 ... val10 (sets values for lut idx)
               hs_info
               hs_tuning ...
               buf_info
               debug_lib_flow <enable/disable>
               log <enable/disable>
               frame_selection <enable/disable>
               dump_selection <opt> <opt> ... (opt can be : params / frame / gyro / hs_debug / stab_orient)
    hdr        lib_info
    rgb_dump   <on/off>
    delayed_display  <enable/disable> - Visualize delayed stream on display (for Hypersmooth)
    sgde_fill_color  <black/green/pink> - Set SGDE fill color (for debugging grid issue)
```

```
Usage: t frw sensor [command]
    reg_read <register address>
    reg_dump_all
    reg_write <register address> <value>
```

```
Usage: t frw gp_ipc [command]
    command:
         enable         Enable IPC
         disable        Disable IPC
         stats          Show IPC statistics
```

```
Usage: t frw mcu fwupdate <filename> [sd|romfs] [force]
                 filecheck <filename>
                 romcheck  <filename>
                 fileload  <filename>
                 romload   <filename>
                 gt_get_mode
                 gt_set_mode [usb/aud]
```

```
Usage: t frw me [command]
         open    opens medit module
         suspend suspend medit module
         resume  resume medit module
         config [start_msec] [end_msec] config medit module
         cb      set callback handler
         start   starts medit job
         cancel  cancel medit job
         tag  [time_msec] add moment tag
         xc       transcoder <FileIndex> <Bitrate> <Width> <Height> [<FRD> <M> <N> <IDR_Int>]
                    where
                       FRD     is the optional Frame Rate Divisor (0-8)
                       IDR_Int is the optional IDR Interval in units of GOPs (1-4)
         xopen    opens transcode module
         xresume  resume transcode module
         xconfig  <FileIndex> <Bitrate> <Width> <Height> configure transcode module
         xstart   starts transcode job
         xsuspend suspend transcode module
         xcancel  cancel current transcode
```

```
Usage: t frw mft [command]
         start              starts record
         stop               stops record
         intv [msec]        interval record enable
         setbr [bps]        set streaming bit rate
         setgop [gop_n]     set streaming gop N
         setidr [idr]       set streaming idr interval
         setwin [size enum] set streaming enc window
         setbcid            set BCID
         text               insert text
         md_open            open _mft_md instance
         md_dereg [src_id]  deregister metadata src
         md_start           start metadata session record
         md_stop            stop metadata session record
         md_send            send metadata periodically
         recording          show whether video is being recorded to the SD
         show               show statistics of captured and encoder a/v frames
         frate              frame rate received by mft
         log [fifo_full]    dump debug log to sdcard C:\debug_xxxxxxxx.log immediate OR on specified condition
         vbuf_profile [on/off/show] on/off : enable/disable video buffer profile, show : display video profile data
         jpeg_qual [1-99] on/off : JPEG Compression Ratio
```

```
Usage: t frw imgcap [command]
    fd         <enable/disable>
    3dnr       <enable/disable>
    ltm        <enable/disable>
    gp_ltm     <enable/disable>
    mfnr       <enable/disable>
    dzoom      <enable/disable>
               test_dzoom_repeat repeat_no<1-100> interval_in_ms<0-1000>
               dzoom_eff_val <0-256>
    ae_info    <enable/disable>
    clean_raw  <enable/disable>
    eis        <enable/disable>
               info
               algo <fotonation/hypersmooth/lowlatency/stub/disable/unset>
               gp ...
               first_sample_time
               strength min_val(0.0 to 1.0) max_val(0.0 to 1.0)
               strengthlut idx (makes lut idx the current lut)
               strengthlut idx val0 val1 ... val10 (sets values for lut idx)
               hs_info
               hs_tuning ...
               buf_info
               debug_lib_flow <enable/disable>
               log <enable/disable>
               frame_selection <enable/disable>
               dump_selection <opt> <opt> ... (opt can be : params / frame / gyro / hs_debug / stab_orient)
    hdr        lib_info
    rgb_dump   <on/off>
    delayed_display  <enable/disable> - Visualize delayed stream on display (for Hypersmooth)
    sgde_fill_color  <black/green/pink> - Set SGDE fill color (for debugging grid issue)
```

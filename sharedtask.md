<script>document.title = "Field Matters | Call for papers";</script>

<head>
<meta property="og:title" content="Field Matters | Call for papers">
<meta property="og:description" content="The first workshop on applying NLP to field linguistics">
<meta property="og:image" content="https://github.com/field-matters/field-matters.github.io/blob/main/logo.jpg?raw=true">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css">
<script src="https://unpkg.com/wavesurfer.js"></script>
<script src="https://unpkg.com/wavesurfer.js@6.1.0/dist/plugin/wavesurfer.regions.js"></script>
  <link href="https://use.fontawesome.com/releases/v5.6.1/css/all.css" rel="stylesheet">
  <style> 
    .frame{
      width: max-content;
      margin: auto;
      height: 60px;
      position: relative;
      text-decoration: none;
      margin-top:10px;
    }
    
    .btn{
      text-decoration: none;
      border: 0;
      background-color: inherit;
      height: 40px;
      flex-direction: column;
      color: #2a2424;
      font-size: 30px;
    }
    
    .tg  {
      border:none;
      border-collapse:collapse;
      border-spacing:0;
    }
    .tg td{
      color: #2a2424;
      border-style:solid;
      border-width:0px;
      font-family:Arial, sans-serif;
      font-size:14px;
      overflow:hidden;
      padding:10px 5px;
      word-break:normal;
    }
    .tg th{
      border-style:solid;
      color: #2a2424;
      border-width:0px;
      font-family:Arial, sans-serif;
      font-size:14px;
      font-weight:normal;
      overflow:hidden;
      padding:10px 5px;
      word-break:normal;
    }
    .tg .tg-1wig{
      font-weight:bold;
      text-align:left;
      vertical-align:top;
      background-color:inherit;
    }
    .tg .tg-4vsk{
      background-color:hsla(200, 50%, 70%, 0.1);
      border-color:inherit;
      color:#000000;
      text-align:left;
      vertical-align:top
    }
    .tg .tg-0pky{
      border-color:inherit;
      background-color:inherit;
      text-align:left;
      vertical-align:top
    }
  </style>
</head>

## Field Matters: Speech Processing Tasks

This year, we offer two shared tasks on processing speech in field linguistic recordings.
Linguistic data collection involves recording narratives, wordlists, and grammatical enqueting. Narratives are a priceless source of linguistic, anthropological and socio-cultural information. Wordlists are basic building blocks for everyone who studies the language, and for those who learn languages. Enquetes provide a unique view on what is plausible, and what is forbidden in a language, providing researchers with negative examples to adjust their theoretical models.

Automatic speech processing will optimize the time spent on language data treatment. In the shared tasks, we seek for means to reduce such a monotonous routine. We propose two tasks, targeting two stages of linguistic recordings annotation: diarization and transcription (ASR).

## Diarization
Before transcribing the speech, we want to identify who does speak and when. Unlike common speech corpora, field records often contain multiple types of noise, such as wind howling, animal shrikes and other. In addition to that, there are two or more participants who interact using two languages.
 
We are particularly interested in finding the native speakers' segments. In the training data, only the target language is annotated as well as the overall number of speakers, and only this information gets taken into account in the automatic evaluation during the coding period. Evaluation of the held-out dataset where both under-resourced language and high-resourced language chunks are annotated will be held after the submission deadline.

## ASR
You are expected to provide the transcription of a given recording of a under-resourced language speech. 

We don't expect an  accurate transcription to be accomplished at this time. Linguistically and phonetically motivated errors receive fewer penalty than uninterpretable ones. That is, predicting /s/ instead of /z/ gets fewer penalty than predicting /s/ instead of /b/.
We don't also pay attention to word boundaries detection. Therefore predictions "the cat sat on the mat" and "theca tsaton them at" are considered equal.

## Important links
+ [Github repository](https://github.com/field-matters/ST2022)
+ [Registration](TBA) - TBA

## Important dates
+ May, 16:  Introductory data
+ May, 30:  Train 1
+ Middle of June:  Train 2
+ Early July:  Competition

## Data sample
<div>
 <div id="waveform"></div>
 <script>
    wavesurfer = WaveSurfer.create({
        container: '#waveform',
        waveColor: '#49b2e1',
        progressColor: '#ae1917',
        cursorColor: '#2a2424',
        plugins: [
            WaveSurfer.regions.create({
                regions: [
                    {
                        start: 0,
                        end: 2.1,
                        color: 'hsla(200, 50%, 70%, 0.1)',
                        drag: false,
                        resize: false,
                    },
                    {
                        start: 4,
                        end: 7,
                        color: 'hsla(200, 50%, 70%, 0.1)',
                        drag: false,
                        resize: false,
                    }
                ]
            }),
        ]
    });
    wavesurfer.load('audio/example-even.wav');
 </script>
 <div class="frame">
     <a href="" class="btn" onclick="wavesurfer.skipBackward(); event.preventDefault()" style="text-decoration: none">
   <i class="bi bi-skip-start-circle"></i>
  </a>
      <a href="" class="btn" onclick="wavesurfer.playPause(); event.preventDefault()" style="text-decoration: none">
  <i class="bi bi-play-circle"></i>
  </a>
      <a href="" class="btn" onclick="wavesurfer.skipForward(); event.preventDefault()" style="text-decoration: none">
   <i class="bi bi-skip-end-circle"></i>
  </a>
  </div>
  <table class="tg">
  <thead>
    <tr>
      <th class="tg-1wig">start</th>
      <th class="tg-1wig">end</th>
      <th class="tg-1wig">transcription</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="tg-4vsk">00:00:00.019</td>
      <td class="tg-4vsk">00:00:02.321</td>
      <td class="tg-4vsk">ekmu unideji enikrɨn oram</td>
    </tr>
    <tr>
      <td class="tg-0pky">00:00:02.640</td>
      <td class="tg-0pky">00:00:03.900</td>
      <td class="tg-0pky"><i>(a linguist speaking)</i></td>
    </tr>
    <tr>
      <td class="tg-4vsk">00:00:04.036</td>
      <td class="tg-4vsk">00:00:07.330</td>
      <td class="tg-4vsk">ekmu uni unirin oram</td>
    </tr>
  </tbody>
  </table>
</div> 

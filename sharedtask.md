<script>document.title = "Field Matters | Shared Task";</script>

<head>
<meta property="og:title" content="Field Matters | Shared Task">
<meta property="og:description" content="The first workshop on applying NLP to field linguistics">
<meta property="og:image" content="https://github.com/field-matters/field-matters.github.io/blob/main/logo.jpg?raw=true">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css">
<script src="https://unpkg.com/wavesurfer.js"></script>
<script src="https://unpkg.com/wavesurfer.js@6.1.0/dist/plugin/wavesurfer.regions.js"></script>
  <link href="https://use.fontawesome.com/releases/v5.6.1/css/all.css" rel="stylesheet">
  <style> 
     summary::-webkit-details-marker{display:none;}
    summary::-moz-list-bullet{list-style-type:none;}
    summary::marker{display:none;} 
    summary {
         padding: .3em 1.5em .3em .6em;
         display:inline-block;
         font-size:1.4em;
         cursor: pointer;
         position: relative;
            }
     summary:before {
         right: .3em;
         top: .4em;
         color: transparent;
         background:                url("data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjM0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIzNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cGF0aCBkPSJNOC41OSAxNi4zNGw0LjU4LTQuNTktNC41OC00LjU5TDEwIDUuNzVsNiA2LTYgNnoiLz48L3N2Zz4=") no-repeat 50% 50% / 1em 1em;
         width: 1em;
         height: 1em;  
         content: "";
         position: absolute;
         transition: transform .5s;
            }
         details[open] > summary:before {
                         transform: rotateZ(90deg);
                                        }
      summary ~ * {
         padding:0 1em 0 1em;
                   }
      details[open] summary ~ *{ 
         animation: sweep .5s ease-in-out;
                                }
      @keyframes sweep {
          0%    {opacity: 0;}
          100%  {opacity: 1;}
                       }
      summary:focus {
        outline:0;
        box-shadow: inset 0 0 1px rgba(0,0,0,0.3), inset 0 0 2px rgba(0,0,0,0.3);
      }
      details{
       display:block;
       margin-bottom: .5rem;
       border: 0; 
      }       
    
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
</head>
## Field Matters: Speech Processing Tasks

### What's new?
#### June, 2
+ Train 1 data is now out
+ We fixed some problems in the previous release (the markup is now in IPA)
+ The notebooks with baseline solutions for the both tasks are published

#### May, 17
+ Pilot data is out

## Description

This year, we offer two shared tasks on processing speech in field linguistic recordings.
Linguistic data collection involves recording narratives, wordlists, and grammatical enqueting. Narratives are a priceless source of linguistic, anthropological and socio-cultural information. Wordlists are basic building blocks for everyone who studies the language, and for those who learn languages. Enquetes provide a unique view on what is plausible, and what is forbidden in a language, providing researchers with negative examples to adjust their theoretical models.

Automatic speech processing will optimize the time spent on language data treatment. In the shared tasks, we seek for means to reduce such a monotonous routine. We propose two tasks, targeting two stages of linguistic recordings annotation: diarization and transcription (ASR).

## Diarization
Before transcribing the speech, we want to identify who does speak and when. Unlike common speech corpora, field records often contain multiple types of noise, such as wind howling, animal shrikes and other. In addition to that, there are two or more participants who interact using two languages.
 
We are particularly interested in finding the native speakers' segments. In the training data, only the target language is annotated as well as the overall number of speakers, and only this information gets taken into account in the automatic evaluation during the coding period. Evaluation of the held-out dataset where both under-resourced language and high-resourced language chunks are annotated will be held after the submission deadline.

<details>
    <summary>Pilot data</summary>
    <p>
      <ul>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://files.deeppavlov.ai/field-matters/releases/demo/dia_data.csv" download>dia_data.csv</a> &mdash; pilot dataset for the Diarization track </li> 
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://files.deeppavlov.ai/field-matters/releases/demo/sound.zip" download>sound.zip</a> &mdash; an archive containing the files referenced in pilot dataset</li>
      </ul>
    </p>
</details>
<details>
    <summary>Train 1 data</summary>
    <p>
      <ul>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://raw.githubusercontent.com/field-matters/ST2022/main/dia_data_train_1.csv" download>dia_data_train_1.csv</a> &mdash; Train 1 dataset for the Diarization track</li> 
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="ссылка на архив диа" download>sound.zip</a> &mdash; an archive containing the files referenced in the dataset TBA</li>
      </ul>
    </p>
</details>
<details >
    <summary>Baseline solution</summary>
    <p>
      <ul>
        <li>Our baseline for ASR is based on the model wav2vec2.</li>
        <li>For diarization task we will measure weighted Jaccard error rate. Weights for native speakers of under-resoursed languages and linguists differ. The omit of a segment segment will also weight more than a false detected segment.</li>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://raw.githubusercontent.com/field-matters/ST2022/main/diarization_baseline.ipynb" download>diarization_baseline.ipynb</a></li>
      </ul>
    </p>
</details>

## ASR
You are expected to provide the transcription of a given recording of a under-resourced language speech. 

We don't expect an  accurate transcription to be accomplished at this time. Linguistically and phonetically motivated errors receive fewer penalty than uninterpretable ones. That is, predicting /s/ instead of /z/ gets fewer penalty than predicting /s/ instead of /b/.
We don't also pay attention to word boundaries detection. Therefore predictions "the cat sat on the mat" and "theca tsaton them at" are considered equal.

<details>
    <summary>Data</summary>
    <p>
      <ul>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://files.deeppavlov.ai/field-matters/releases/demo/asr_data.csv" download>asr_data.csv</a> &mdash; pilot dataset for the ASR track</li> 
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://files.deeppavlov.ai/field-matters/releases/demo/sound.zip" download>sound.zip</a> &mdash; an archive containing the files referenced in pilot dataset</li>
      </ul>
    </p>
</details>
<details>
    <summary>Train 1 data</summary>
    <p>
      <ul>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://raw.githubusercontent.com/field-matters/ST2022/main/asr_data_train_1.csv" download>asr_data_train_1.csv</a> &mdash; Train 1 dataset for the ASR track</li>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="ссылка на архив аср" download>sound.zip</a> &mdash; an archive containing the files referenced in the dataset TBA</li>
      </ul>
    </p>
</details>
<details >
    <summary>Baseline solution</summary>
    <p>
      <ul>
        <li>As a baseline for diarization task, we take pyannote-audio.</li>
        <li>For ASR task we will measure phonetic error rate with weights based on phonetic similarity between a  recognised phomene and a right answer.</li>
        <li style="list-style-type: none;"><i class="fa fa-download" aria-hidden="true"></i> &nbsp; <a href="https://raw.githubusercontent.com/field-matters/ST2022/main/asr_baseline.ipynb" download>asr_baseline.ipynb</a></li>
      </ul>
    </p>
</details>

## Important links
+ [Github repository](https://github.com/field-matters/ST2022)
+ [Registration](https://forms.gle/oZY7h1R71xzNDGEN8)

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

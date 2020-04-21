---
title: "Theoretical Computer Science Reduction Notation Mnemonic"
author: Jacob Strieb
date: April 16, 2020
description: A tactic I use to remember the meaning of theoretical computer science notation for describing reductions
...


# Computer Science Reduction Notation Mnemonic

By [Jacob Strieb](https://jstrieb.github.io)

Published on [April 21, 2020](/posts/reduction-notation/)

---

Reductions are one of the most important concepts in theoretical computer
science. If one problem can be effectively recast as an instance of another via
a reduction, they are related, and in some cases equivalent. Since much of
academic computer science revolves around studying the complexity of
computational problems, understanding the ways in which seemingly different
problems relate to one another is critical.

When a computational problem $X$ "reduces" to another problem $Y$, a Turing
machine that computes $X$ can be written using one or more calls to a Turing
machine that computes $Y$.[^1] The commonly-used notation for this is:

$$ X \leq Y $$

In my introductory theoretical computer science course, several flavors of
reductions have been introduced. However, I have found it difficult to remember
the reduction notation. Specifically, if $X$ reduces to $Y$, I have trouble
remembering that this means computing $X$ can be made to rely on computing $Y$.
The prevalence of this confusing notation in the course materials and academic
literature motivated finding a reliable way to remember its meaning.

My tactic has been to imagine a description for each turing machine ($M_X$ and
$M_Y$) side-by-side, with the "$\leq$" symbol overlaid between them,
representing the definition for $M_Y$ zooming in on the call to $M_Y$ in $M_X$.
A poorly-rendered example diagram can be seen below.

<!-- TODO: Figure out how to embed the SVG such that it is still allowed to be
styled by the global CSS -->
<svg
   xmlns:dc="http://purl.org/dc/elements/1.1/"
   xmlns:cc="http://creativecommons.org/ns#"
   xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
   xmlns:svg="http://www.w3.org/2000/svg"
   xmlns="http://www.w3.org/2000/svg"
   xmlns:sodipodi="http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd"
   xmlns:inkscape="http://www.inkscape.org/namespaces/inkscape"
   width="16.615837cm"
   height="9.9633818cm"
   viewBox="0 0 6.5416681 3.9225911"
   version="1.1"
   id="SVGRoot"
   inkscape:version="0.92.3 (2405546, 2018-03-11)"
   sodipodi:docname="diagram_notext.svg">
  <sodipodi:namedview
     id="base"
     pagecolor="#ffffff"
     bordercolor="#666666"
     borderopacity="1.0"
     inkscape:pageopacity="0.0"
     inkscape:pageshadow="2"
     inkscape:zoom="1.4"
     inkscape:cx="243.5908"
     inkscape:cy="227.86937"
     inkscape:document-units="px"
     inkscape:current-layer="layer1"
     showgrid="true"
     inkscape:window-width="1920"
     inkscape:window-height="1013"
     inkscape:window-x="-9"
     inkscape:window-y="-9"
     inkscape:window-maximized="1"
     units="cm"
     objecttolerance="10"
     gridtolerance="10"
     guidetolerance="10"
     showguides="true"
     inkscape:guide-bbox="true"
     fit-margin-top="0"
     fit-margin-left="0"
     fit-margin-right="0"
     fit-margin-bottom="0">
    <inkscape:grid
       type="xygrid"
       id="grid1442"
       spacingx="0.26041667"
       spacingy="0.26041667"
       dotted="false"
       enabled="true"
       visible="true"
       originx="-0.24479073"
       originy="-3.6302089" />
  </sodipodi:namedview>
  <defs
     id="defs883">
    <inkscape:path-effect
       effect="powerstroke"
       id="path-effect820"
       is_visible="true"
       offset_points="1,0.005208335"
       sort_points="true"
       interpolator_type="CubicBezierJohan"
       interpolator_beta="0.2"
       start_linecap_type="zerowidth"
       linejoin_type="extrp_arc"
       miter_limit="4"
       end_linecap_type="zerowidth" />
  </defs>
  <metadata
     id="metadata886">
    <rdf:RDF>
      <cc:Work
         rdf:about="">
        <dc:format>image/svg+xml</dc:format>
        <dc:type
           rdf:resource="http://purl.org/dc/dcmitype/StillImage" />
        <dc:title></dc:title>
        <dc:creator>
          <cc:Agent>
            <dc:title>Jacob Strieb</dc:title>
          </cc:Agent>
        </dc:creator>
      </cc:Work>
    </rdf:RDF>
  </metadata>
  <g
     id="layer1"
     inkscape:groupmode="layer"
     inkscape:label="Layer 1"
     transform="translate(-0.24479073,-3.4472004)">
    <rect
       style="opacity:1;fill-opacity:1;stroke-width:0.03125;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="rect816"
       width="2.6041675"
       height="2.6041675"
       x="0.26041573"
       y="4.749999"
       rx="0.052083332"
       ry="0.052083332" />
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.5208325,5.5312495 H 2.6041664"
       id="path830"
       inkscape:connector-curvature="0" />
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.5208325,5.7916662 H 2.6041664"
       id="path832"
       inkscape:connector-curvature="0" />
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.5208325,6.052083 H 2.6041664"
       id="path834"
       inkscape:connector-curvature="0" />
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.5208325,6.5729165 H 2.6041664"
       id="path838"
       inkscape:connector-curvature="0" />
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.5208325,6.8333332 H 2.6041664"
       id="path840"
       inkscape:connector-curvature="0" />
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.5208325,7.09375 H 2.6041664"
       id="path842"
       inkscape:connector-curvature="0" />
    <ellipse
       style="opacity:1;fill-opacity:1;stroke-width:0.02083333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       id="path902"
       cx="0.91145831"
       cy="6.312501"
       rx="0.46395874"
       ry="0.19061559" />
    <rect
       y="4.749999"
       x="4.166666"
       height="2.6041675"
       width="2.6041675"
       id="rect1000"
       style="opacity:1;fill-opacity:1;stroke-width:0.03125;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
       rx="0.052083332"
       ry="0.052083332" />
    <path
       inkscape:connector-curvature="0"
       id="path1002"
       d="M 4.4270827,5.5312495 H 6.5104166"
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" />
    <path
       inkscape:connector-curvature="0"
       id="path1004"
       d="M 4.4270827,5.7916662 H 6.5104166"
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" />
    <path
       inkscape:connector-curvature="0"
       id="path1006"
       d="M 4.4270827,6.052083 H 6.5104166"
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" />
    <path
       inkscape:connector-curvature="0"
       id="path1008"
       d="M 4.4270827,6.5729165 H 6.5104166"
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" />
    <path
       inkscape:connector-curvature="0"
       id="path1010"
       d="M 4.4270827,6.8333332 H 6.5104166"
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" />
    <path
       inkscape:connector-curvature="0"
       id="path1012"
       d="M 4.4270827,7.09375 H 6.5104166"
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1" />
    <g
       id="g8545"
       class="text">
      <g
         id="text854"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.34722233px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.01562501;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="M">
        <path
           id="path8512"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.01562501"
           d="m 0.85077828,5.2312659 -0.001695,0.0017 q -0.0167847,-0.00102 -0.052219,-0.00102 -0.036282,0 -0.052219,0.00102 l -0.001526,-0.00153 v -0.011529 l 0.001695,-0.0017 q 0.0172933,-0.00102 0.0198364,-0.0017 0.004917,-0.00136 0.005764,-0.00627 0.002204,-0.012207 0.002204,-0.052558 V 5.0430741 l -0.0378079,0.077481 q -0.003221,0.00644 -0.0220405,0.047472 l -0.0310262,0.067817 h -0.0113593 q -0.008816,-0.021023 -0.0239054,-0.053067 l -0.0237359,-0.050354 -0.04442,-0.0924 v 0.1176622 q 0,0.040351 0.002204,0.052558 8.4771e-4,0.00492 0.005764,0.00627 0.002543,6.782e-4 0.0198364,0.0017 l 0.001695,0.0017 v 0.011529 l -0.001695,0.00153 q -0.0194973,-0.00102 -0.036282,-0.00102 -0.0194973,0 -0.0391642,0.00102 l -0.001695,-0.00153 v -0.011529 l 0.001695,-0.0017 q 0.0172933,-0.00102 0.0198364,-0.0017 0.004917,-0.00136 0.005764,-0.00627 0.002204,-0.012207 0.002204,-0.052558 v -0.089688 q 0,-0.040351 -0.002204,-0.052558 -8.4771e-4,-0.00492 -0.005764,-0.00627 -0.002543,-6.782e-4 -0.0198364,-0.0017 l -0.001695,-0.0017 V 4.994246 l 0.001695,-0.00153 q 0.0176324,0.00102 0.0445896,0.00102 0.0206841,0 0.0361125,-0.00102 0.005595,0.012885 0.015937,0.036282 l 0.0108507,0.023397 0.0539144,0.1127456 0.02594,-0.052558 0.0405206,-0.086636 q 0.007121,-0.015428 0.0139025,-0.03323 0.0191583,0.00102 0.0257704,0.00102 0.0332303,0 0.0508627,-0.00102 l 0.001695,0.00153 v 0.011698 l -0.001695,0.00153 q -0.0172933,0.00102 -0.0198364,0.0017 -0.004917,0.00136 -0.005764,0.00627 -0.002204,0.012207 -0.002204,0.052558 v 0.089688 q 0,0.040351 0.002204,0.052558 8.4771e-4,0.00492 0.005764,0.00627 0.002543,6.782e-4 0.0198364,0.0017 l 0.001695,0.0017 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text858"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.22704318px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.01021695;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="X">
        <path
           id="path8509"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.01021695"
           d="m 0.99737091,5.2939499 -0.001109,0.00111 -0.0226156,-3.326e-4 q -0.005543,-1.109e-4 -0.0194007,3.326e-4 -0.003326,-0.0041 -0.0108644,-0.01807 l -0.0230591,-0.042681 -0.008758,0.012527 q -0.0166291,0.023835 -0.0308193,0.048224 -0.0051,-3.326e-4 -0.0101992,-3.326e-4 -0.0103101,0 -0.0150771,3.326e-4 l -0.001109,-0.00111 v -0.0071 l 0.001109,-0.00122 q 0.009091,-6.652e-4 0.0109752,-0.00188 0.003326,-0.00211 0.0150771,-0.01807 l 0.0145228,-0.019622 q 8.8688e-4,-0.00111 0.0177377,-0.023946 l -0.008425,-0.014855 -0.013525,-0.023392 q -0.0144119,-0.024833 -0.0219505,-0.029378 -0.00255,-0.00155 -0.005321,-0.00155 -0.002217,0 -0.006873,3.326e-4 l -0.001441,-0.00111 -8.8689e-4,-0.00588 9.9775e-4,-0.00166 q 0.0156314,-0.00321 0.0402425,-0.00887 0.006984,0.00455 0.0144119,0.016407 0.003548,0.00576 0.0110861,0.019733 l 0.0125273,0.023281 0.0144119,-0.021064 q 0.0178486,-0.026163 0.0231699,-0.035586 0.004545,4.435e-4 0.00898,4.435e-4 0.007428,0 0.0150771,-4.435e-4 l 0.001109,0.00111 v 0.00732 l -0.001109,0.00111 q -0.007649,1.108e-4 -0.0101992,0.00166 -0.002439,0.00155 -0.009645,0.010532 -0.007206,0.00898 -0.0189572,0.024944 -0.006541,0.00887 -0.015964,0.022061 0.005543,0.010199 0.0158531,0.028713 l 0.0141902,0.024389 q 0.0117513,0.020177 0.0147445,0.022837 0.003104,0.00255 0.009977,0.00255 l 0.001109,0.00111 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text862"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.17861269px;line-height:125%;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.00803757;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="Run M">
        <path
           id="path8488"
           style="stroke-width:0.00803757"
           d="m 0.7045065,6.3525736 -8.7213e-4,8.721e-4 q -6.105e-4,0 -0.003314,-8.72e-5 -0.0119482,-4.361e-4 -0.0149135,-4.361e-4 -0.004448,0 -0.0141285,5.233e-4 -3.4885e-4,-0.00209 -0.003314,-0.00698 l -0.0216289,-0.036106 -0.009681,-0.014739 q -0.001831,-0.0027 -0.005146,-0.00532 l 9.5934e-4,-0.00297 q 0.002006,8.72e-5 0.002965,8.72e-5 0.008547,0 0.0134308,-0.0027 0.004448,-0.00244 0.008198,-0.00855 0.00375,-0.0061 0.00375,-0.014565 0,-0.014739 -0.0109889,-0.019885 -0.005233,-0.00244 -0.0152623,-0.00244 -0.004361,0 -0.008372,6.977e-4 -8.7213e-4,0.00855 -8.7213e-4,0.029129 v 0.045612 q 0,0.020757 0.001134,0.027036 4.3606e-4,0.00253 0.002965,0.00323 0.001308,3.489e-4 0.010204,8.722e-4 l 8.7213e-4,8.721e-4 v 0.00584 l -7.8492e-4,8.721e-4 q -0.008721,-5.233e-4 -0.0268617,-5.233e-4 -0.0187508,0 -0.0268617,5.233e-4 l -8.7213e-4,-7.849e-4 v -0.00593 l 8.7213e-4,-8.721e-4 q 0.008896,-5.233e-4 0.0102039,-8.722e-4 0.002529,-6.977e-4 0.002965,-0.00323 0.001134,-0.00628 0.001134,-0.027036 v -0.046136 q 0,-0.020757 -0.001134,-0.027036 -4.3607e-4,-0.00253 -0.002965,-0.00323 -0.001308,-3.489e-4 -0.0102039,-8.722e-4 L 0.58511159,6.23658 V 6.23065 l 8.7213e-4,-7.849e-4 q 0.008547,5.233e-4 0.0268617,5.233e-4 0.01064,0 0.0172682,-2.617e-4 0.0131692,-5.233e-4 0.0197102,-5.233e-4 0.0150879,0 0.0221522,0.0027 0.009506,0.00366 0.0127331,0.012384 0.00157,0.00427 0.00157,0.010117 0,0.023722 -0.0266872,0.033664 0.004361,0.00733 0.009245,0.014826 l 0.0134308,0.020669 q 0.011861,0.018315 0.0157856,0.020844 0.002006,0.00131 0.005582,0.00131 l 8.7213e-4,8.721e-4 z"
           inkscape:connector-curvature="0" />
        <path
           id="path8490"
           style="stroke-width:0.00803757"
           d="m 0.8119532,6.3524864 -8.7213e-4,8.721e-4 q -0.013082,-4.361e-4 -0.0164833,-4.361e-4 -0.002878,0 -0.008547,1.745e-4 -0.005669,2.616e-4 -0.00846,2.616e-4 l -6.977e-4,-6.977e-4 q 6.977e-4,-0.00715 6.977e-4,-0.013605 -0.004535,0.0034 -0.0158728,0.014477 -0.005669,0.00218 -0.0121226,0.00218 -0.0117738,0 -0.0185764,-0.00637 -0.006803,-0.00645 -0.006803,-0.018489 0,-0.00148 1.7442e-4,-0.00628 1.7443e-4,-0.0048 1.7443e-4,-0.00924 v -0.011163 q 0,-0.017268 -0.001308,-0.020059 -8.7213e-4,-0.00174 -0.00375,-0.00218 -0.001047,-1.745e-4 -0.007675,-4.361e-4 l -8.7213e-4,-8.721e-4 v -0.00488 l 8.7213e-4,-9.593e-4 q 0.0166577,-0.00148 0.0337515,-0.00724 l 0.001919,0.00113 q -0.001134,0.014477 -0.001134,0.026774 v 0.017007 q 0,0.011948 7.8492e-4,0.016309 8.7213e-4,0.00523 0.004099,0.00794 0.003314,0.0027 0.008809,0.0027 0.006803,0 0.0119482,-0.00436 0.004884,-0.00436 0.005146,-0.00994 1.7443e-4,-0.00427 1.7443e-4,-0.00532 v -0.015611 q 0,-0.017094 -0.001308,-0.020059 -7.8492e-4,-0.00174 -0.003663,-0.00218 -0.001047,-1.745e-4 -0.007675,-4.361e-4 l -9.5935e-4,-8.721e-4 v -0.00488 l 9.5935e-4,-9.593e-4 q 0.0165705,-0.00148 0.0337515,-0.00724 l 0.001831,0.00113 q -0.001134,0.013082 -0.001134,0.026774 v 0.027385 q 0,0.018402 0.001047,0.020844 5.2328e-4,0.00122 0.001744,0.00157 0.002093,6.105e-4 0.00907,0.00105 l 9.5935e-4,8.722e-4 z M 0.7613695,6.2641394 Z m 0,0.095586 z"
           inkscape:connector-curvature="0" />
        <path
           id="path8492"
           style="stroke-width:0.00803757"
           d="m 0.92175465,6.3525736 -8.7214e-4,9.593e-4 q -0.009593,-6.105e-4 -0.0162217,-6.105e-4 -0.006105,0 -0.0177915,6.105e-4 l -8.7213e-4,-8.721e-4 q 0.00157,-0.019449 0.00157,-0.030001 v -0.017094 q 0,-0.02128 -0.0153495,-0.02128 -0.008024,0 -0.0125587,0.00549 -0.003837,0.00462 -0.003837,0.00933 v 0.016309 q 0,0.022588 0.001134,0.027734 6.977e-4,0.00305 0.0101167,0.00323 l 8.7213e-4,8.722e-4 v 0.00532 l -8.7213e-4,8.721e-4 q -0.007413,-5.233e-4 -0.0221522,-5.233e-4 -0.0156112,0 -0.0238092,6.105e-4 l -8.7213e-4,-8.721e-4 v -0.00532 l 8.7213e-4,-8.721e-4 q 0.008372,-2.617e-4 0.0103784,-0.00131 0.001744,-7.85e-4 0.001919,-0.00419 6.105e-4,-0.011338 6.105e-4,-0.024332 v -0.012472 q 0,-0.017443 -0.001308,-0.020059 -8.7213e-4,-0.00174 -0.00375,-0.00218 -0.001047,-1.745e-4 -0.007588,-4.361e-4 l -8.7213e-4,-8.721e-4 v -0.00488 l 8.7213e-4,-9.593e-4 q 0.0156984,-0.00148 0.0330538,-0.00724 l 0.001919,0.00113 -1.7442e-4,0.014652 0.0150007,-0.012559 q 0.005756,-0.00235 0.0126459,-0.00235 0.0138669,0 0.0207567,0.00837 0.005582,0.0068 0.005582,0.019972 0,0.00148 -3.4886e-4,0.012123 -3.4885e-4,0.01064 -3.4885e-4,0.015175 0,0.013169 4.3607e-4,0.016832 4.3606e-4,0.00358 0.002006,0.00454 0.00157,9.593e-4 0.00907,0.00113 l 7.8492e-4,8.721e-4 z"
           inkscape:connector-curvature="0" />
        <path
           id="path8494"
           style="stroke-width:0.00803757"
           d="m 1.1425786,6.3525736 -8.722e-4,8.721e-4 q -0.00863,-5.233e-4 -0.026862,-5.233e-4 -0.018664,0 -0.026862,5.233e-4 l -7.849e-4,-7.849e-4 v -0.00593 l 8.721e-4,-8.721e-4 q 0.0089,-5.233e-4 0.010204,-8.722e-4 0.00253,-6.977e-4 0.00297,-0.00323 0.00113,-0.00628 0.00113,-0.027036 v -0.058956 l -0.019449,0.039856 q -0.00166,0.00331 -0.011338,0.02442 l -0.01596,0.034885 h -0.00584 q -0.00454,-0.010814 -0.012297,-0.027298 l -0.01221,-0.025902 -0.02285,-0.047531 v 0.060526 q 0,0.020757 0.00113,0.027036 4.36e-4,0.00253 0.00297,0.00323 0.00131,3.489e-4 0.010204,8.722e-4 l 8.721e-4,8.721e-4 v 0.00593 l -8.721e-4,7.849e-4 q -0.01003,-5.233e-4 -0.0186637,-5.233e-4 -0.0100295,0 -0.0201463,5.233e-4 l -8.7214e-4,-7.849e-4 v -0.00593 l 8.7214e-4,-8.721e-4 q 0.008896,-5.233e-4 0.0102039,-8.722e-4 0.002529,-6.977e-4 0.002965,-0.00323 0.001134,-0.00628 0.001134,-0.027036 v -0.046136 q 0,-0.020757 -0.001134,-0.027036 -4.3606e-4,-0.00253 -0.002965,-0.00323 -0.001308,-3.489e-4 -0.0102039,-8.722e-4 L 0.97704784,6.23658 V 6.23065 l 8.7214e-4,-7.849e-4 q 0.00907,5.233e-4 0.0229371,5.233e-4 0.01064,0 0.018576,-5.233e-4 0.00288,0.00663 0.0082,0.018664 l 0.00558,0.012035 0.027734,0.057997 0.013344,-0.027036 0.020844,-0.044566 q 0.00366,-0.00794 0.00715,-0.017094 0.00986,5.233e-4 0.013257,5.233e-4 0.017094,0 0.026164,-5.233e-4 l 8.722e-4,7.849e-4 v 0.00602 l -8.722e-4,7.849e-4 q -0.0089,5.233e-4 -0.010204,8.722e-4 -0.00253,6.977e-4 -0.00297,0.00323 -0.00113,0.00628 -0.00113,0.027036 v 0.046136 q 0,0.020757 0.00113,0.027036 4.361e-4,0.00253 0.00297,0.00323 0.00131,3.489e-4 0.010204,8.722e-4 l 8.722e-4,8.721e-4 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text866"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.10716756px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.00482254;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="Y">
        <path
           id="path8485"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.00482254"
           d="m 1.2071148,6.3084184 q -0.00827,0.011251 -0.018106,0.027577 -0.00555,0.00921 -0.00612,0.011774 -3.14e-4,0.00136 -3.14e-4,0.00392 v 0.00518 q 0,0.015332 9.419e-4,0.017059 4.186e-4,7.326e-4 0.0012,9.419e-4 0.00131,3.663e-4 0.00644,6.803e-4 l 5.233e-4,5.233e-4 v 0.00351 l -5.233e-4,5.233e-4 q -0.00518,-3.14e-4 -0.016117,-3.14e-4 -0.011198,0 -0.016117,3.14e-4 l -4.71e-4,-4.709e-4 v -0.00356 L 1.158975,6.375553 q 0.00513,-3.14e-4 0.00644,-6.803e-4 7.85e-4,-2.093e-4 0.0012,-9.419e-4 9.419e-4,-0.00173 9.419e-4,-0.017059 v -0.00617 q 0,-0.00199 -0.00822,-0.015908 -0.00837,-0.014181 -0.013344,-0.019257 -0.00241,-0.00246 -0.00324,-0.00277 -8.373e-4,-3.663e-4 -0.00392,-3.663e-4 l -5.756e-4,-5.756e-4 v -0.00293 l 5.232e-4,-5.756e-4 q 0.012768,-0.00251 0.016379,-0.00356 0.00272,0.00131 0.00487,0.0034 0.00445,0.00434 0.011931,0.019361 l 0.00685,0.01371 q 0.00309,-0.00497 0.011774,-0.019989 l 0.00581,-0.010413 q 9.419e-4,-0.00173 0.00256,-0.00476 h 0.00764 l 5.233e-4,5.233e-4 z m -0.032077,0.075457 z m 0,-0.080899 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text916"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:1.32262599px;line-height:125%;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.05951818;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="X ≤ Y">
        <path
           id="path8515"
           style="fill-opacity:1;stroke-width:0.05951818"
           d="m 2.822667,4.4634192 -0.00646,0.00646 -0.1317459,-0.00194 Q 2.6521722,4.467294 2.5714455,4.4698773 2.5520711,4.4459822 2.5081558,4.3646097 L 2.3738266,4.1159715 2.3228073,4.1889484 q -0.096872,0.1388499 -0.1795361,0.2809289 -0.029707,-0.00194 -0.059415,-0.00194 -0.060061,0 -0.087831,0.00194 l -0.00646,-0.00646 v -0.041332 l 0.00646,-0.0071 q 0.052957,-0.00387 0.063936,-0.010979 0.019374,-0.01227 0.087831,-0.1052676 l 0.084602,-0.114309 Q 2.23756,4.1779696 2.3357236,4.044932 L 2.2866418,3.958393 2.2078525,3.8221264 q -0.083956,-0.1446622 -0.127871,-0.1711406 -0.014854,-0.00904 -0.030999,-0.00904 -0.012916,0 -0.04004,0.00194 l -0.0084,-0.00646 -0.00517,-0.034228 0.00581,-0.00969 q 0.09106,-0.018729 0.2344303,-0.051665 0.040686,0.026478 0.083956,0.09558 0.020666,0.033582 0.064581,0.1149548 l 0.072977,0.1356209 0.083956,-0.1227046 q 0.103976,-0.152412 0.134975,-0.2073061 0.026478,0.00258 0.052311,0.00258 0.04327,0 0.087831,-0.00258 l 0.00646,0.00646 v 0.042624 l -0.00646,0.00646 q -0.044561,6.458e-4 -0.059415,0.00969 -0.014208,0.00904 -0.056186,0.061352 -0.041978,0.052311 -0.1104341,0.145308 -0.038103,0.051665 -0.092997,0.1285169 0.032291,0.059415 0.092351,0.1672657 l 0.082664,0.142079 q 0.068456,0.117538 0.085893,0.1330376 0.018083,0.014854 0.058123,0.014854 l 0.00646,0.00646 z"
           inkscape:connector-curvature="0" />
        <path
           id="path8517"
           style="fill-opacity:1;stroke-width:0.05951818"
           d="M 3.819803,4.3032574 3.1991762,4.0223286 V 3.9228733 L 3.819803,3.6406528 V 3.754316 L 3.3496508,3.9719551 3.819803,4.1895942 Z m 0,0.1646825 H 3.1991762 v -0.11108 H 3.819803 Z"
           inkscape:connector-curvature="0" />
        <path
           id="path8519"
           style="fill-opacity:1;stroke-width:0.05951818"
           d="M 5.041682,3.5870503 Q 4.9396435,3.7259002 4.8182306,3.927394 q -0.068456,0.1136631 -0.07556,0.145308 -0.00387,0.016791 -0.00387,0.048436 v 0.063936 q 0,0.1892233 0.011625,0.2105351 0.00517,0.00904 0.014854,0.011625 0.016145,0.00452 0.079435,0.0084 l 0.00646,0.00646 v 0.04327 l -0.00646,0.00646 q -0.063935,-0.00387 -0.1989105,-0.00387 -0.1382041,0 -0.1989106,0.00387 l -0.00581,-0.00581 v -0.043915 l 0.00646,-0.00646 q 0.06329,-0.00387 0.079435,-0.0084 0.00969,-0.00258 0.014854,-0.011625 0.011625,-0.021312 0.011625,-0.2105351 V 4.108873 q 0,-0.024541 -0.1013927,-0.1963273 -0.1033301,-0.1750155 -0.1646824,-0.2376594 -0.029707,-0.030353 -0.04004,-0.034228 -0.010333,-0.00452 -0.048436,-0.00452 l -0.0071,-0.0071 v -0.036166 l 0.00646,-0.0071 q 0.1575785,-0.030999 0.2021397,-0.043915 0.033582,0.016145 0.060061,0.041978 0.054894,0.053602 0.1472455,0.238951 l 0.084601,0.1692031 Q 4.7303999,3.930623 4.837605,3.7452746 L 4.90929,3.6167577 q 0.011625,-0.021312 0.031645,-0.058769 h 0.094289 l 0.00646,0.00646 z m -0.3958836,0.931263 z m 0,-0.9984276 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text988"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.34722233px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.01562501;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label=":">
        <path
           id="path8506"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.01562501"
           d="m 1.0576655,5.0737613 q 0.01102,0 0.01865,0.00797 0.0078,0.00797 0.0078,0.018819 0,0.01102 -0.0078,0.018989 -0.00763,0.00797 -0.01865,0.00797 -0.01102,0 -0.018819,-0.0078 -0.0078,-0.00797 -0.0078,-0.019158 0,-0.01119 0.0078,-0.018989 0.0078,-0.0078 0.018819,-0.0078 z m 0,0.1096937 q 0.010851,0 0.01865,0.0078 0.0078,0.00763 0.0078,0.019158 0,0.01119 -0.0078,0.018989 -0.0078,0.0078 -0.01865,0.0078 -0.010851,0 -0.018819,-0.0078 -0.0078,-0.00797 -0.0078,-0.018989 0,-0.01119 0.0078,-0.018989 0.0078,-0.00797 0.018819,-0.00797 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text1016"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.34722233px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.01562501;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="M">
        <path
           id="path8503"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.01562501"
           d="m 4.7570286,5.2312659 -0.0017,0.0017 q -0.016785,-0.00102 -0.052219,-0.00102 -0.036282,0 -0.052219,0.00102 l -0.00153,-0.00153 v -0.011529 l 0.0017,-0.0017 q 0.017293,-0.00102 0.019837,-0.0017 0.00492,-0.00136 0.00576,-0.00627 0.0022,-0.012207 0.0022,-0.052558 V 5.0430741 l -0.037808,0.077481 q -0.00322,0.00644 -0.02204,0.047472 l -0.031026,0.067817 h -0.011359 q -0.00882,-0.021023 -0.023905,-0.053067 l -0.023736,-0.050354 -0.04442,-0.0924 v 0.1176622 q 0,0.040351 0.0022,0.052558 8.477e-4,0.00492 0.00576,0.00627 0.00254,6.782e-4 0.019837,0.0017 l 0.0017,0.0017 v 0.011529 l -0.0017,0.00153 q -0.019497,-0.00102 -0.036282,-0.00102 -0.019497,0 -0.039164,0.00102 l -0.0017,-0.00153 v -0.011529 l 0.0017,-0.0017 q 0.017293,-0.00102 0.019836,-0.0017 0.00492,-0.00136 0.00576,-0.00627 0.0022,-0.012207 0.0022,-0.052558 v -0.089688 q 0,-0.040351 -0.0022,-0.052558 -8.478e-4,-0.00492 -0.00576,-0.00627 -0.00254,-6.782e-4 -0.019836,-0.0017 l -0.0017,-0.0017 V 4.994246 l 0.0017,-0.00153 q 0.017632,0.00102 0.04459,0.00102 0.020684,0 0.036112,-0.00102 0.00559,0.012885 0.015937,0.036282 l 0.010851,0.023397 0.053914,0.1127456 0.02594,-0.052558 0.040521,-0.086636 q 0.00712,-0.015428 0.013903,-0.03323 0.019158,0.00102 0.02577,0.00102 0.03323,0 0.050863,-0.00102 l 0.0017,0.00153 v 0.011698 l -0.0017,0.00153 q -0.017293,0.00102 -0.019837,0.0017 -0.00492,0.00136 -0.00576,0.00627 -0.0022,0.012207 -0.0022,0.052558 v 0.089688 q 0,0.040351 0.0022,0.052558 8.477e-4,0.00492 0.00576,0.00627 0.00254,6.782e-4 0.019837,0.0017 l 0.0017,0.0017 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text1020"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.22704318px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.01021695;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label="Y">
        <path
           id="path8500"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.01021695"
           d="m 4.9058385,5.1435116 q -0.017516,0.023835 -0.038358,0.058424 -0.011751,0.019512 -0.012971,0.024944 -6.652e-4,0.00288 -6.652e-4,0.00831 v 0.010975 q 0,0.032482 0.002,0.036141 8.869e-4,0.00155 0.00255,0.002 0.00277,7.76e-4 0.013636,0.00144 l 0.00111,0.00111 v 0.00743 l -0.00111,0.00111 q -0.010975,-6.652e-4 -0.034145,-6.652e-4 -0.023724,0 -0.034145,6.652e-4 l -9.978e-4,-9.978e-4 v -0.00754 l 0.00111,-0.00111 q 0.010864,-6.652e-4 0.013636,-0.00144 0.00166,-4.435e-4 0.00255,-0.002 0.002,-0.00366 0.002,-0.036141 v -0.013082 q 0,-0.00421 -0.017405,-0.033702 -0.017738,-0.030043 -0.02827,-0.040797 -0.0051,-0.00521 -0.00687,-0.00588 -0.00177,-7.76e-4 -0.00831,-7.76e-4 l -0.00122,-0.00122 v -0.00621 l 0.00111,-0.00122 q 0.02705,-0.00532 0.0347,-0.00754 0.00576,0.00277 0.01031,0.00721 0.00942,0.0092 0.025276,0.041018 l 0.014523,0.029046 q 0.00654,-0.010532 0.024944,-0.042349 l 0.012306,-0.022061 q 0.002,-0.00366 0.00543,-0.010088 h 0.016186 l 0.00111,0.00111 z M 4.8378807,5.303373 Z m 0,-0.1713909 z"
           inkscape:connector-curvature="0" />
      </g>
      <g
         id="text1034"
         style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-size:0.34722233px;line-height:125%;font-family:sans-serif;-inkscape-font-specification:'sans-serif Bold';text-align:start;text-anchor:start;opacity:1;fill-opacity:1;stroke-width:0.01562501;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-dashoffset:0;stroke-opacity:1"
         aria-label=":">
        <path
           id="path8497"
           style="font-style:normal;font-variant:normal;font-weight:bold;font-stretch:normal;font-family:'Palatino Linotype';-inkscape-font-specification:'Palatino Linotype Bold';fill-opacity:1;stroke-width:0.01562501"
           d="m 4.9639155,5.0737613 q 0.01102,0 0.01865,0.00797 0.0078,0.00797 0.0078,0.018819 0,0.01102 -0.0078,0.018989 -0.00763,0.00797 -0.01865,0.00797 -0.01102,0 -0.018819,-0.0078 -0.0078,-0.00797 -0.0078,-0.019158 0,-0.01119 0.0078,-0.018989 0.0078,-0.0078 0.018819,-0.0078 z m 0,0.1096937 q 0.010851,0 0.01865,0.0078 0.0078,0.00763 0.0078,0.019158 0,0.01119 -0.0078,0.018989 -0.0078,0.0078 -0.01865,0.0078 -0.010851,0 -0.018819,-0.0078 -0.0078,-0.00797 -0.0078,-0.018989 0,-0.01119 0.0078,-0.018989 0.0078,-0.00797 0.018819,-0.00797 z"
           inkscape:connector-curvature="0" />
      </g>
    </g>
    <path
       style="fill-rule:evenodd;stroke-width:0.05208333;stroke-linecap:round;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 4.4270827,6.3124999 H 6.5104166"
       id="path1036"
       inkscape:connector-curvature="0" />
    <path
       style="fill-rule:evenodd;stroke-width:0.02083333;stroke-linecap:butt;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.90773839,6.1223048 4.204095,4.7500003"
       id="path1040"
       inkscape:connector-curvature="0"
       sodipodi:nodetypes="cc" />
    <path
       style="fill-rule:evenodd;stroke-width:0.02083333;stroke-linecap:butt;stroke-linejoin:miter;stroke-miterlimit:4;stroke-dasharray:none;stroke-opacity:1"
       d="M 0.90401815,6.5026993 4.2059631,7.354167"
       id="path1042"
       inkscape:connector-curvature="0"
       sodipodi:nodetypes="cc" />
  </g>
</svg>


[^1]: If $M_X$ computes $X$ and $M_Y$ computes $Y$, then the way in which $M_X$
      calls $M_Y$ varies depending on the type of reduction under consideration.

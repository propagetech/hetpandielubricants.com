You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | ABOUT US",
      "first_heading": "ABOUT US"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | CONTACT US",
      "first_heading": "CONTACT US"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/47199a09e42d8056913f4a8ecfae0607.css",
    "context": {
      "path": "css/47199a09e42d8056913f4a8ecfae0607.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/c363a15baf9b3719c1570c22b012b369.css",
    "context": {
      "path": "css/c363a15baf9b3719c1570c22b012b369.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "domestic-network.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | DOMESTIC NETWORK",
      "first_heading": "DOMESTIC NETWORK"
    }
  },
  {
    "path": "enquiry.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | ENQUIRY",
      "first_heading": "ENQUIRY"
    }
  },
  {
    "path": "events.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | EVENTS",
      "first_heading": "EVENTS"
    }
  },
  {
    "path": "imgs/02b0d5af3b1e32e92555b7a00f37766e.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/04cd26a7e71848a5ebf8e88a2669b63b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/1287f7add13d513841c0bf8b22b10179.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ccb160305e8b7e48fedee32256c2197.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/254ccda561b42a17cff0dd943d92184f.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex AUTOMATIC 854G",
          "title": ""
        },
        {
          "alt": "Trennex AUTOMATIC 854G",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2e7f1e2c3fd36906f14c1367c8a1fb29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/371cd9c4752fd50d6a72cd0cba994035.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3db2ea75d701d4e0c430cd19e043cdac.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex 3282 Paste",
          "title": ""
        },
        {
          "alt": "Trennex 3282 Paste",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3e39582987706d41db721482687f8a62.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/432b9d93cc1f0eafb161ea9dfdd033be.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex ALSI",
          "title": ""
        },
        {
          "alt": "Trennex ALSI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47fa70c43d0713303bb9d09a1614828e.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fde25e26c3c3ebbd7021137eb4388c6.webp",
    "context": {
      "refs": [
        {
          "alt": "ECO-FRIENDLY PRODUCTS AND CERTIFICATIONS",
          "title": ""
        },
        {
          "alt": "ECO-FRIENDLY PRODUCTS AND CERTIFICATIONS",
          "title": ""
        },
        {
          "alt": "ECO-FRIENDLY PRODUCTS AND CERTIFICATIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/518bebc087bf355e605341aaf18bc71b.webp",
    "context": {
      "refs": [
        {
          "alt": "Geiger + Co. announces collaboration with Hetpan Die Lubricants in Foundry Planet News",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/559c3a19605577c1de701e525f44e029.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "Geiger + Co. Schmierstoff-Chemie GmbH",
          "title": ""
        },
        {
          "alt": "In Technical Collaboration With",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/564e03a308c5eecb594189c9970f7543.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bcaeb74b55be9956e8414e68352489b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/5deafa72dd035dddd02858eb9fc679a8.webp",
    "context": {
      "refs": [
        {
          "alt": "Hetpan Overseas",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61717066d778a582b0dcddd7773545dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6399d0a2e1027120e46407278f52114a.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Storage Facility",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63eae86234cb663e094085b82fc3ff08.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Spezialwachs VM 1620 (Special wax)",
          "title": ""
        },
        {
          "alt": "Trennex Spezialwachs VM 1620 (Special wax)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6fb8615f288d761529438361b6f48c06.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/778ce088b476a3490d58caa02448e0e9.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7d6f79c40b6a567ec068416a86c81324.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e5f7945f34a51ccec82c30a43b40dac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/827e0b7ce19aeb5c0690443ae2ab48b5.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex AL",
          "title": ""
        },
        {
          "alt": "Trennex AL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84db7f1daa7a3bf66d98d5731cc87698.webp",
    "context": {
      "refs": [
        {
          "alt": "HETPAN PRODUCTS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8657dee27fc77e9533edfbad0302e807.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex 3000",
          "title": ""
        },
        {
          "alt": "Trennex 3000",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c35f9e4990ad94fa993113034e14359.webp",
    "context": {
      "refs": [
        {
          "alt": "HETPAN DIE LUBRICANTS is formed with a single focus mission of catering to emerging India to manufac",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91c2f0e5fbce216478da8136e09b1078.webp",
    "context": {
      "refs": [
        {
          "alt": "HETPAN EVENTS",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/929870d839a37b166c98be7713f57cee.webp",
    "context": {
      "refs": [
        {
          "alt": "FOR YOUR SUCCESS",
          "title": ""
        },
        {
          "alt": "FOR YOUR SUCCESS",
          "title": ""
        },
        {
          "alt": "FOR YOUR SUCCESS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/952c897037f24eba35400b2373defcaa.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex 899/11,\u00a0Trennex 899",
          "title": ""
        },
        {
          "alt": "Trennex 899/11,\u00a0Trennex 899",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98d048157833e846710898487cf450dc.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9d83cf6c37875b60641ce90f7517d89d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a1dc6ec12bb054fb5da3b76e7eabe6b9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a490f104164a21f043b30ed302f2b591.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b0dc1228f2c289cb6d03084943206cf0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b5721aca08135b6e061e17fae4016faa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b9832ce1e3dabce86326d05cacb89f43.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b9eefd470554fbaa6a5dcbe2963dbca3.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ba81fcfc30facb8fdcd6765b68e1a848.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bc26b60905a3cde8bd01d4872187a47a.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/be7b3ee99b12fa939c35a0e1c9b6c367.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c005ed5ce8580543ce8d9d4896389027.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1ec2177520de19f711646ff95f865e6.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/cc61e668d568e0dfce99016c260a52ea.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce6a3494a81832f44454c3ae6e57ccb2.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex AUTOMATIC 3099/Trennex AUTOMATIC 899+899/11",
          "title": ""
        },
        {
          "alt": "Trennex AUTOMATIC 3099/Trennex AUTOMATIC 899+899/11",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cff17ef8799eb1a22d4fe9c5d60caf04.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Automatic 3099",
          "title": ""
        },
        {
          "alt": "Trennex Automatic 3099",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d17c178e151b08e107c58f80e55c36fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "COMING SOON",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3fd537092c79340c3f99e6926388d9b.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d42a529a5cced3d757ddf62f2e790c47.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Lab",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df1e8ccddfa18610137a61d6b3b485cd.webp",
    "context": {
      "refs": [
        {
          "alt": "Trennex Cu Paste",
          "title": ""
        },
        {
          "alt": "Trennex Cu Paste",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f65916702ff970fd41ecc29b21ba5ff6.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f7960816d3fc81736f6de0cdc755da7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imported-from-germany.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | TRENNEX PRODUCTS IMPORTED FROM GERMANY",
      "first_heading": "TRENNEX PRODUCTS IMPORTED FROM GERMANY"
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | HOME",
      "first_heading": "In Technical Collaboration WithTHE BEST OF GERMAN TECHNOLOGY, NOW MADE IN INDIA."
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e734a79111d3ae5022fadd97f4b4570.js",
    "context": {
      "path": "js/3e734a79111d3ae5022fadd97f4b4570.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js",
    "context": {
      "path": "js/a626b42d5e9f3bebfd9624955f0d721b.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  },
  {
    "path": "manufactured-in-india.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | MANUFACTURED IN INDIA",
      "first_heading": "MANUFACTURED IN INDIA"
    }
  },
  {
    "path": "products.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | PRODUCTS OVERVIEW",
      "first_heading": "PRODUCTS OVERVIEW"
    }
  },
  {
    "path": "resources.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | RESOURCES",
      "first_heading": "RESOURCES"
    }
  },
  {
    "path": "technical-collaboration.html",
    "context": {
      "title": "HETPAN DIE LUBRICANTS | TECHNICAL COLLABORATION",
      "first_heading": "TECHNICAL COLLABORATION"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.
<script>
import * as monaco from "monaco-editor/esm/vs/editor/editor.api";

export default {
  setup() {
    const TsLanguage = {
      defaultToken: "invalid",
      tokenPostfix: ".ts",
      keywords: [
        "abstract",
        "as",
        "break",
        "case",
        "catch",
        "class",
        "continue",
        "const",
        "constructor",
        "debugger",
        "declare",
        "default",
        "delete",
        "do",
        "else",
        "enum",
        "export",
        "extends",
        "false",
        "finally",
        "for",
        "from",
        "function",
        "get",
        "if",
        "implements",
        "import",
        "in",
        "infer",
        "instanceof",
        "interface",
        "is",
        "keyof",
        "let",
        "module",
        "namespace",
        "never",
        "new",
        "null",
        "package",
        "private",
        "protected",
        "public",
        "readonly",
        "require",
        "global",
        "return",
        "set",
        "static",
        "super",
        "switch",
        "symbol",
        "this",
        "throw",
        "true",
        "try",
        "type",
        "typeof",
        "unique",
        "var",
        "void",
        "while",
        "with",
        "yield",
        "async",
        "await",
        "of",
      ],
      typeKeywords: [
        "any",
        "boolean",
        "number",
        "object",
        "string",
        "undefined",
      ],
      operators: [
        "<=",
        ">=",
        "==",
        "!=",
        "===",
        "!==",
        "=>",
        "+",
        "-",
        "**",
        "*",
        "/",
        "%",
        "++",
        "--",
        "<<",
        "</",
        ">>",
        ">>>",
        "&",
        "|",
        "^",
        "!",
        "~",
        "&&",
        "||",
        "??",
        "?",
        ":",
        "=",
        "+=",
        "-=",
        "*=",
        "**=",
        "/=",
        "%=",
        "<<=",
        ">>=",
        ">>>=",
        "&=",
        "|=",
        "^=",
        "@",
      ],

      symbols: /[=><!~?:&|+\-*\\^%]+/,
      escapes:
        /\\(?:[abfnrtv\\"']|x[0-9A-Fa-f]{1,4}|u[0-9A-Fa-f]{4}|U[0-9A-Fa-f]{8})/,
      digits: /\d+(_+\d+)*/,
      octaldigits: /[0-7]+(_+[0-7]+)*/,
      binarydigits: /[0-1]+(_+[0-1]+)*/,
      hexdigits: /[[0-9a-fA-F]+(_+[0-9a-fA-F]+)*/,
      regexpctl: /[(){}[\]$^|\-*+?.]/,
      regexpesc:
        /\\(?:[bBdDfnrstvwWn0\\/]|@regexpctl|c[A-Z]|x[0-9a-fA-F]{2}|u[0-9a-fA-F]{4})/,

      tokenizer: {
        root: [
          [/[{}]/, "delimiter.bracket"],
          {
            include: "common",
          },
        ],

        common: [
          [
            /[a-z_$][\w$]*/,
            {
              cases: {
                "@typeKeywords": "keyword",

                "@keywords": "keyword",

                "@default": "identifier",
              },
            },
          ],
          [/[A-Z][\w$]*/, "type.identifier"],
          {
            include: "@whitespace",
          },

          [
            /\/(?=([^\\/]|\\.)+\/([gimsuy]*)(\s*)(\.|;|,|\)|\]|\}|$))/,
            {
              token: "regexp",

              bracket: "@open",

              next: "@regexp",
            },
          ],
          [/[()[\]]/, "@brackets"],
          [/[<>](?!@symbols)/, "@brackets"],
          [/!(?=([^=]|$))/, "delimiter"],

          [
            /@symbols/,
            {
              cases: {
                "@operators": "delimiter",

                "@default": "",
              },
            },
          ],
          [/(@digits)[eE]([-+]?(@digits))?/, "number.float"],
          [/(@digits)\.(@digits)([eE][-+]?(@digits))?/, "number.float"],
          [/0[xX](@hexdigits)n?/, "number.hex"],
          [/0[oO]?(@octaldigits)n?/, "number.octal"],
          [/0[bB](@binarydigits)n?/, "number.binary"],
          [/(@digits)n?/, "number"],
          [/[;,.]/, "delimiter"],
          [/"([^"\\]|\\.)*$/, "string.invalid"],
          [/'([^'\\]|\\.)*$/, "string.invalid"],
          [/"/, "string", "@string_double"],
          [/'/, "string", "@string_single"],
          [/`/, "string", "@string_backtick"],
        ],

        whitespace: [
          [/[ \t\r\n]+/, ""],
          [/\/\*\*(?!\/)/, "comment.doc", "@jsdoc"],
          [/\/\*/, "comment", "@comment"],
          [/\/\/.*$/, "comment"],
        ],

        comment: [
          [/[^/*]+/, "comment"],
          [/\*\//, "comment", "@pop"],
          [/[/*]/, "comment"],
        ],

        jsdoc: [
          [/[^/*]+/, "comment.doc"],
          [/\*\//, "comment.doc", "@pop"],
          [/[/*]/, "comment.doc"],
        ],

        regexp: [
          [
            /(\{)(\d+(?:,\d*)?)(\})/,
            [
              "regexp.escape.control",
              "regexp.escape.control",
              "regexp.escape.control",
            ],
          ],
          [
            /(\[)(\^?)(?=(?:[^\]\\/]|\\.)+)/,
            [
              "regexp.escape.control",
              {
                token: "regexp.escape.control",

                next: "@regexrange",
              },
            ],
          ],
          [
            /(\()(\?:|\?=|\?!)/,
            ["regexp.escape.control", "regexp.escape.control"],
          ],
          [/[()]/, "regexp.escape.control"],
          [/@regexpctl/, "regexp.escape.control"],
          [/[^\\/]/, "regexp"],
          [/@regexpesc/, "regexp.escape"],
          [/\\\./, "regexp.invalid"],
          [
            /(\/)([gimsuy]*)/,
            [
              {
                token: "regexp",
                bracket: "@close",
                next: "@pop",
              },
              "keyword.other",
            ],
          ],
        ],

        regexrange: [
          [/-/, "regexp.escape.control"],
          [/\^/, "regexp.invalid"],
          [/@regexpesc/, "regexp.escape"],
          [/[^\]]/, "regexp"],
          [
            /\]/,
            {
              token: "regexp.escape.control",
              next: "@pop",
              bracket: "@close",
            },
          ],
        ],

        string_double: [
          [/[^\\"]+/, "string"],
          [/@escapes/, "string.escape"],
          [/\\./, "string.escape.invalid"],
          [/"/, "string", "@pop"],
        ],

        string_single: [
          [/[^\\']+/, "string"],
          [/@escapes/, "string.escape"],
          [/\\./, "string.escape.invalid"],
          [/'/, "string", "@pop"],
        ],

        string_backtick: [
          [
            /\$\{/,
            {
              token: "delimiter.bracket",

              next: "@bracketCounting",
            },
          ],
          [/[^\\`$]+/, "string"],
          [/@escapes/, "string.escape"],
          [/\\./, "string.escape.invalid"],
          [/`/, "string", "@pop"],
        ],

        bracketCounting: [
          [/\{/, "delimiter.bracket", "@bracketCounting"],
          [/\}/, "delimiter.bracket", "@pop"],
          {
            include: "common",
          },
        ],
      },
    };

    const JavaScriptLanguage = {
      defaultToken: "invalid",

      tokenPostfix: ".js",

      keywords: [
        "break",
        "case",
        "catch",
        "class",
        "continue",
        "const",
        "constructor",
        "debugger",
        "default",
        "delete",
        "do",
        "else",
        "export",
        "extends",
        "false",
        "finally",
        "for",
        "from",
        "function",
        "get",
        "if",
        "import",
        "in",
        "instanceof",
        "let",
        "new",
        "null",
        "return",
        "set",
        "super",
        "switch",
        "symbol",
        "this",
        "throw",
        "true",
        "try",
        "typeof",
        "undefined",
        "var",
        "void",
        "while",
        "with",
        "yield",
        "async",
        "await",
        "of",
      ],

      typeKeywords: [],

      operators: TsLanguage.operators,

      symbols: TsLanguage.symbols,
      escapes: TsLanguage.escapes,
      digits: TsLanguage.digits,
      octaldigits: TsLanguage.octaldigits,
      binarydigits: TsLanguage.binarydigits,
      hexdigits: TsLanguage.hexdigits,
      regexpctl: TsLanguage.regexpctl,
      regexpesc: TsLanguage.regexpesc,
      tokenizer: TsLanguage.tokenizer,
    };
    monaco.languages.register({ id: "javascript" });
    monaco.languages.register({ id: "js" });
    monaco.languages.setMonarchTokensProvider("js", JavaScriptLanguage);
    monaco.languages.setMonarchTokensProvider("javascript", JavaScriptLanguage);
  },
  data() {
    return {
      content: this.code,
      sandboxProxies: new WeakMap(),
      editor: null,
    };
  },
  props: ["code", "editorIndex"],
  methods: {
    compile() {
      const textarea = this.$refs.output;
      textarea.value =
        "Webworker travaille à l'exécution de votre code. Si rien n'est renvoyé, vérifiez le console.log du navigateur et voyez si vous n'avez pas fait une bêtise.";
      const textcontent = monaco.editor
        .getModels()
        [this.editorIndex].getValue();

      const worker = new Worker("worker.js");
      worker.postMessage({ code: textcontent });

      setTimeout(() => {
        console.log("woker terminated after 5000 millisec");
        worker.terminate(); //in case the student wrote infinite loop or something else thats stupid
      }, 5000);

      worker.onmessage = function (event) {
        if (event.data.status === "success") {
          textarea.value = event.data.message;
          console.log("Code executed successfully");
        } else if (event.data.status === "error") {
          textarea.value = event.data.message;
          console.error(event.data.message);
        }
      };
    },
  },
  mounted() {
    const editorElement = this.$refs.editor;
    this.editor = monaco.editor.create(editorElement, {
      value: this.content,
      language: "javascript",
      automaticLayout: true,
      fontSize: "18px",
      theme: "vs-dark",
    });
  },
};
</script>
<template>
  <div class="flex-container">
    <div style="width: 60%; height: 100%">
      <div id="editor" ref="editor"></div>
    </div>
    <div style="width: 35%">
      <textarea ref="output" readonly></textarea>
      <button style="vertical-align: middle" @click="compile()">
        <span>Compile</span>
      </button>
    </div>
  </div>
</template>
<style scoped>
#editor {
  width: 60%;
  height: 60%;
  position: absolute !important;
}
textarea {
  height: 250px;
  width: 100%;
}
button {
  display: inline-block;
  border-radius: 4px;
  background-color: #feb322ff;
  border: none;
  text-align: center;
  font-size: 1rem;
  font-weight: bold;
  width: 70%;
  height: 30px;
  transition: all 0.5s;
  cursor: pointer;
  margin-top: 2%;
}

button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

button span:after {
  content: "\00bb";
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

button:hover span {
  padding-right: 25px;
}

button:hover span:after {
  opacity: 1;
  right: 0;
}
</style>

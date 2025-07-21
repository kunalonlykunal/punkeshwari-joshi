<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Punkeshwari Joshi | Portfolio</title>

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- React & ReactDOM -->
    <script crossorigin src="https://unpkg.com/react@18/umd/react.development.js"></script>
    <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"></script>

    <!-- Framer Motion -->
    <script src="https://unpkg.com/framer-motion/dist/framer-motion.umd.js"></script>
  </head>

  <body class="bg-gray-100 text-gray-900">
    <div id="root"></div>

    <script type="text/javascript">
      const { motion } = window['framer-motion'];
      const { useEffect } = React;

      function App() {
        useEffect(() => {
          document.title = "Punkeshwari Joshi | Portfolio";
        }, []);

        const projects = [
          { title: "UI Design Kit", desc: "Modern UI Kit for dashboards." },
          { title: "Portfolio v2", desc: "Animated, responsive portfolio." },
          { title: "E-commerce UI", desc: "Shopping interface with cart logic." },
          { title: "Blog CMS", desc: "Minimal blog with markdown support." },
        ];

        const skills = [
          "HTML5", "CSS3", "JavaScript", "React",
          "Figma", "Tailwind CSS", "UI/UX Design"
        ];

        return (
          React.createElement("main", { className: "p-6 font-sans" },
            React.createElement("section", {
              className: "text-center py-20 bg-white shadow-md rounded-2xl"
            },
              React.createElement(motion.h1, {
                className: "text-5xl font-bold mb-4",
                initial: { opacity: 0, y: -50 },
                animate: { opacity: 1, y: 0 },
                transition: { duration: 0.6 }
              }, "Hi, I'm Punkeshwari Joshi"),
              React.createElement("p", {
                className: "text-lg mb-6 text-gray-600"
              }, "Frontend Developer | UI/UX Designer | Creative Thinker"),
              React.createElement("a", {
                href: "#",
                className: "bg-blue-600 hover:bg-blue-700 text-white px-5 py-2 rounded-full"
              }, "Download Resume")
            ),

            React.createElement("section", { className: "mt-20" },
              React.createElement("h2", {
                className: "text-3xl font-semibold mb-6 text-center"
              }, "Projects"),
              React.createElement("div", {
                className: "grid gap-6 md:grid-cols-2"
              },
                projects.map((project, idx) =>
                  React.createElement("div", {
                    key: idx,
                    className: "bg-white p-6 rounded-xl shadow"
                  },
                    React.createElement("h3", { className: "text-xl font-bold mb-2" }, project.title),
                    React.createElement("p", { className: "text-gray-600" }, project.desc)
                  )
                )
              )
            ),

            React.createElement("section", { className: "mt-20" },
              React.createElement("h2", {
                className: "text-3xl font-semibold mb-6 text-center"
              }, "Skills & Tools"),
              React.createElement("div", {
                className: "flex flex-wrap justify-center gap-4 text-sm text-gray-700"
              },
                skills.map((skill, idx) =>
                  React.createElement("span", {
                    key: idx,
                    className: "bg-white px-4 py-2 rounded-full shadow"
                  }, skill)
                )
              )
            ),

            React.createElement("section", {
              className: "mt-20 text-center"
            },
              React.createElement("h2", {
                className: "text-3xl font-semibold mb-4"
              }, "Let's Connect"),
              React.createElement("p", {
                className: "text-gray-600 mb-4"
              }, "punkeshwari.joshi@gmail.com"),
              React.createElement("a", {
                href: "mailto:punkeshwari.joshi@gmail.com",
                className: "bg-green-600 hover:bg-green-700 text-white px-5 py-2 rounded-full"
              }, "Contact Me")
            ),

            React.createElement("footer", {
              className: "mt-20 text-center text-gray-400 text-sm"
            }, "© 2025 Punkeshwari Joshi. All rights reserved.")
          )
        );
      }

      const root = ReactDOM.createRoot(document.getElementById("root"));
      root.render(React.createElement(App));
    </script>
  </body>
</html>

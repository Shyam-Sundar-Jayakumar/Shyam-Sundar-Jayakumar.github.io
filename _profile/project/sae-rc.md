## SAE Aero Design Challenge

* [Documentation](https://acrlakshman.github.com/profileio)
* Highlights:
  * Design of fixed wing RC Plane for payload carrying mission using CATIA.
  * CFD Analysis on the plane to estimate its aerodynamic forces and structural integrity using Ansys. 
  * Development of the plane for real life testing with appropriate component selection
  * Placed in the 'Top 13' in the SAE Aero Design Challenge conducted in India

---

## Run locally

```sh
git clone https://github.com/acrlakshman/profileio

cd profileio
yarn && yarn start
```

---

## [profileio-resume](https://github.com/acrlakshman/profileio-resume)

```go
package main

import (
	"io/ioutil"
	"log"
	"os"
	"os/exec"

	"github.com/acrlakshman/profileio-resume/profileio"
)

func main() {
	jsonData, _ := ioutil.ReadFile("./profile_resume.json")
	profileio.ProfileIO(jsonData)

	app := "xelatex"
	if !commandExists(app) {
		app = "pdflatex"
		if !commandExists(app) {
			log.Print("Cannot compile resume.tex")
			os.Exit(0)
		}
	}

	os.Chdir("./resume")
	cmd := exec.Command(app, "resume.tex")
	_, err := cmd.Output()
	if err != nil {
		log.Printf("%v", err)
	}
}

func commandExists(cmd string) bool {
	_, err := exec.LookPath(cmd)

	return err == nil
}
```

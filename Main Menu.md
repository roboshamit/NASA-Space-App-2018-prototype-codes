# NASA-Space-App-2018-prototype-codes
This is the file for the codes of our current prototype on 15/10/2018
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Mainmenu : MonoBehaviour {

    // Load Scene 01 when start button is pressed
    public void StartGame()
    {
        SceneManager.LoadScene("Map");
    }

    // Load Trophy Room scene when trophy room button is pressed
    public void GotoNASADATA()
    {
        SceneManager.LoadScene("NasaData");
    }

    // Reset All Player Preferences data to start earn trophies again
    public void ResetPlayerPrefs()
    {
        PlayerPrefs.DeleteAll();
    }

}

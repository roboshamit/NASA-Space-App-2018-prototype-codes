# NASA-Space-App-2018-prototype-codes
This is the file for the codes of our current prototype on 15/10/2018
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
using UnityEngine.UI;

public class Nasadatamanager : MonoBehaviour {


    // References to data to control
    public GameObject data1, data2, data3;

    // Variables to contain Player Prefs values
     int data1Got, data2Got, data3Got;

    // Use this for initialization
    void Start()
    {

        // Getting Player Prefs values to make sure you got
        // particular data
        /*
        data1Got = PlayerPrefs.GetInt("data1Got");
        data2Got = PlayerPrefs.GetInt("data2Got");
        data3Got = PlayerPrefs.GetInt("data3Got");

        
          if (data1Got == 1)
              data1.SetActive(true);
          else
              data1.SetActive(false);


          if (data2Got == 1)
              data2.SetActive(true);
          else
              data2.SetActive(false);

          if (data3Got == 1)
              data3.SetActive(true);
          else
              data3.SetActive(false);
          */
              
    }


    public void OpenURLSea()
    {
        Application.OpenURL("https://sealevel.nasa.gov/");
        Debug.Log("is this working?");
    }
    public void OpenURLClim()
    {
        Application.OpenURL("https://climate.nasa.gov/");
        Debug.Log("is this working?");
    }
    public void OpenURLCryo()
    {
        Application.OpenURL("https://ice.nasa.gov/");
        Debug.Log("is this working?");
    }
    public void Mainmenu()
    {
        SceneManager.LoadScene("MainMenu");
    }
}

# NASA-Space-App-2018-prototype-codes
This is the file for the codes of our current prototype on 15/10/2018
Time management to control flow of the quiz questions
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;
using UnityEngine.SceneManagement;

public class TimeManager : MonoBehaviour {

    public float startingTime;
    private Text theText;
    int currentSceneIndex;
    //private PauseMenu thePauseMenu;
   // public GameObject gameOverScreen;
    
    // Use this for initialization
    void Start()
    {
        theText = GetComponent<Text>();
        currentSceneIndex = SceneManager.GetActiveScene().buildIndex;
        //	thePauseMenu = FindObjectOfType<PauseMenu> ();
    }

    // Update is called once per frame
    void Update()
    {
        //	if(thePauseMenu.isPaused)
        //		return;
        startingTime -= Time.deltaTime;
        if (startingTime <= 0)
        {
            SceneManager.LoadScene(currentSceneIndex + 1);
           // gameOverScreen.SetActive(true);
            startingTime = 0;
        }
        theText.text = "" + Mathf.Round(startingTime);
        if (startingTime <= 30 && startingTime > 10)
        {
            theText.color = Color.yellow;
        }
        else if (startingTime <= 10)
        {
            theText.color = Color.red;

        }
    }

}

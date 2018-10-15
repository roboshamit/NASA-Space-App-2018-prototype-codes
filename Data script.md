# NASA-Space-App-2018-prototype-codes
This is the file for the codes of our current prototype on 15/10/2018
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.UI;

public class DataScript : MonoBehaviour {
    public static int data = 100;
    public GameObject datao;
    Text datat;
    // Use this for initialization
    void Start () {
        datat= GetComponent<Text>();
    }
	
	// Update is called once per frame
	void Update () {
        datat.text = "" + data;
    }
}

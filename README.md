# music_groups_micro


A. Clear instructions for how to programmatically REQUEST data from the microservice you implemented. Include an example call. Do not advise your teammate to use your test program or require them to, your teammate must write all of their own code.

To programmatically request data from the microservice, you need first have both the microservice and your main program running in their own dedicated terminals. After that, if you want to request the microservice to save your groups in tracks_effects.json, then you need to send three strings as parameters (one above the other) to the request.txt file (so that the microservice can read that data). For example, for the save option your program would send something like this to request.txt.; save
                                                                             tracks_effects.json
                                                                             {
                                                                              "groups": [
                                                                                  {
                                                                                      "group_id": 1,
                                                                                      "group_name": "Drums",
                                                                                      "items": [
                                                                                          "Kick",
                                                                                          "Snare",
                                                                                          "Hi-Hat"
                                                                                      ]
                                                                                  },
                                                                                 
                                                                                  }
                                                                              ]
                                                                          }

Where "save", "tracks_effects.json", and the groups I pasted above, are actually on their own individual lines, one above the other and with no commas seperating them. The example call I pasted above was incorrectly reformatted (the parameters to request.txt should be one above the other).
If your program wants to restore your most recent backup group, the you would send the single parameter string "restore" to the request.txt file. For example, your main program would send this to request.txt; restore

If your program wants to delete your recent backup group, the you would send two string parameters (one above the other) to the request.txt file. For example, your main program would send this to request.txt; delete
                                                                                 backup
Again GitHub incorrectly reformatted my example call to request.txt. The parameters really should be one above the other, not next to eachother on the same line.The main program will receive this data from the response.txt file.


B. Clear instructions for how to programmatically RECEIVE data from the microservice you implemented. Include an example call.
reIf your main program wants to receive the data that the microservice sends, after you requested save to the microservice, then you would look at the content of the response.txt file and extract those strings from that text file. The microservice sends its responses to response.txt. For example the response.txt file might look something like;      success
                                                                                Track/effect groups saved successfully
                                                                                Backup_Name=backup
Again GitHub incorrectly reformatted my example call where the main program receives data from the microservice. The parameters really should be one above the other, not next to eachother on the same line. The main program will receive this data from the response.txt file.

If your main program wants to receive the data that the microservice sends, after you requested restore to the microservice, then you would look at the content of the response.txt file and extract those strings from that text file. For example the response.txt file might look something like;      success
                          Track/effect groups restored successfully
                          {"groups": [{"group_id": 1, "group_name": "Drums", "items": ["Kick", "Snare", "Hi-Hat"]}, {"group_id": 2, "group_name": "Synths", "items": ["Lead", "Pad", "Bass"]}], "backup_name": "backup", "timestamp": "2025-02-19T14:30:00"}

Again GitHub incorrectly reformatted my example call where the main program receives data from the microservice. The parameters really should be one above the other, not next to eachother on the same line. The main program will receive this data from the response.txt file.


If your main program wants to receive the data that the microservice sends, after you requested delete to the microservice, then you would look at the content of the response.txt file and extract those strings from that text file. For example the response.txt file might look something like;      success
                          Track/effect groups deleted successfully
Again GitHub incorrectly reformatted my example call where the main program receives data from the microservice. The parameters really should be one above the other, not next to eachother on the same line.


C. UML sequence diagram showing how requesting and receiving data works. Make it detailed enough that your teammate (and your grader) will understand.


![UML diagrams (1)](https://github.com/user-attachments/assets/a67a5c96-154c-4b45-b2e9-e8a6fce7961e)



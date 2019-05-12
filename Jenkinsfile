{
    "variables":{
        "secret" :"",
        "access" : ""
      },
    "builders": [
       {
        "type": "amazon-ebs",
        "access_key": "{{user `access`}}",
        "secret_key": "{{user `secret`}}",
        "region": "us-west-2",
        "instance_type": "t2.micro",
        "ami_name": "ami_3",
        "source_ami": "ami-005bdb005fb00e791",
        "ssh_username": "ubuntu"
       }
    ],
    "provisioners":[
        {
            "type": "shell",
            "inline": [
                "sudo apt-get update",
                "sudo apt-get install git",
                "sudo apt-get install tree" 
            ]
        }
    ]
}
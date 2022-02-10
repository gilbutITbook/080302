using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class RouletteController : MonoBehaviour
{
    float rotSpeed = 0;  // 회전 속도   

    void Start()
    {
    }

    void Update()
    {
        // 마우스가 눌리면 회전 속도를 설정한다
        if (Input.GetMouseButtonDown(0))
        {
            this.rotSpeed = 10;
        }

        // 회전 속도만큼 룰렛을 회전 시킨다
        transform.Rotate(0, 0, this.rotSpeed);

        // 룰렛을 감속시킨다(추가)
        this.rotSpeed *= 0.96f;
    }
}

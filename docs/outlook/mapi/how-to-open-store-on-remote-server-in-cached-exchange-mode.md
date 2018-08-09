---
title: Abra un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 25f896038e25823f1fe49d3cafbd5835a0a43f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817009"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Abra un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange

**Hace referencia a**: Outlook 
  
Este tema contiene un ejemplo de código en C++ que se muestra cómo usar el indicador **MDB_ONLINE** para abrir un almacén de mensajes en el servidor remoto cuando Microsoft Outlook 2010 o Microsoft Outlook 2013 está en modo caché de Exchange. 
  
El modo de intercambio en caché permite que Outlook 2010 y Outlook 2013 para usar una copia local del buzón de un usuario mientras Outlook 2010 o 2013 Outlook mantiene una conexión en línea a una copia remota de buzón de correo del usuario en el servidor de Exchange remoto. Cuando Outlook 2010 o 2013 de Outlook se ejecuta en modo caché de Exchange, de forma predeterminada, las soluciones MAPI que inicie sesión en la misma sesión también están conectadas en el almacén de mensajes almacenados en caché. Los datos que se tiene acceso y los cambios que se realizan se realizan con la copia local del buzón.
  
Un proveedor de servicio o cliente puede invalidar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto estableciendo el bit de **MDB_ONLINE** en el parámetro *ulFlags* al llamar a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). Después de que el almacén se ha abierto correctamente en el servidor remoto para esa sesión, puede usar [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir elementos o carpetas en el almacén remoto. 
  
No se puede abrir un almacén de Exchange en modo de caché y en modo sin caché al mismo tiempo en la misma sesión MAPI. Si ya ha abierto el almacén de mensajes almacenados en caché, ya sea debe cerrar el almacén antes de que se abra con esta marca, o se abre una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante el uso de esta marca.
  
El ejemplo de código siguiente muestra cómo llamar a **IMAPISession::OpenMsgStore** con el indicador **MDB_ONLINE** establecido en el parámetro *ulFlags* para abrir el almacén predeterminado en el servidor remoto. 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a>Vea también

- [Información sobre las adiciones de MAPI](about-mapi-additions.md) 
- [Constantes MAPI](mapi-constants.md)
- [Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)


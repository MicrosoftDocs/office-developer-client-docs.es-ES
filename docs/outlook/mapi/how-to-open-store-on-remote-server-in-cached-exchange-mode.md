---
title: Abra un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: 7c1b3d3d5eed6bc991f8e4fd702fa197d610c104
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584803"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="ba1ea-103">Abra un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="ba1ea-103">Open a store on the remote server when Outlook is in Cached Exchange Mode</span></span>

<span data-ttu-id="ba1ea-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba1ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba1ea-105">Este tema contiene un ejemplo de código en C++ que se muestra cómo usar el indicador **MDB_ONLINE** para abrir un almacén de mensajes en el servidor remoto cuando Microsoft Outlook 2010 o Microsoft Outlook 2013 está en modo caché de Exchange.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-105">This topic contains a code sample in C++ that shows how to use the **MDB_ONLINE** flag to open a message store on the remote server when Microsoft Outlook 2010 or Microsoft Outlook 2013 is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="ba1ea-106">El modo de intercambio en caché permite que Outlook 2010 y Outlook 2013 para usar una copia local del buzón de un usuario mientras Outlook 2010 o 2013 Outlook mantiene una conexión en línea a una copia remota de buzón de correo del usuario en el servidor de Exchange remoto.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-106">Cached Exchange Mode permits Outlook 2010 and Outlook 2013 to use a local copy of a user's mailbox while Outlook 2010 or Outlook 2013 maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="ba1ea-107">Cuando Outlook 2010 o 2013 de Outlook se ejecuta en modo caché de Exchange, de forma predeterminada, las soluciones MAPI que inicie sesión en la misma sesión también están conectadas en el almacén de mensajes almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-107">When Outlook 2010 or Outlook 2013 is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="ba1ea-108">Los datos que se tiene acceso y los cambios que se realizan se realizan con la copia local del buzón.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="ba1ea-109">Un proveedor de servicio o cliente puede invalidar la conexión con el almacén de mensajes local y abrir el almacén en el servidor remoto estableciendo el bit de **MDB_ONLINE** en el parámetro *ulFlags* al llamar a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="ba1ea-109">A client or service provider can override the connection to the local message store and open the store on the remote server by setting the bit for **MDB_ONLINE** in the  *ulFlags*  parameter when calling [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span> <span data-ttu-id="ba1ea-110">Después de que el almacén se ha abierto correctamente en el servidor remoto para esa sesión, puede usar [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir elementos o carpetas en el almacén remoto.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-110">After the store has been successfully opened on the remote server for that session, you can use [IMAPISession::OpenEntry](imapisession-openentry.md) to open items or folders on the remote store.</span></span> 
  
<span data-ttu-id="ba1ea-111">No se puede abrir un almacén de Exchange en modo de caché y en modo sin caché al mismo tiempo en la misma sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-111">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="ba1ea-112">Si ya ha abierto el almacén de mensajes en modo caché, debe cerrar el almacén antes de abrirlo con esta marca o abrir una nueva sesión MAPI donde puede abrir el almacén de Exchange en el servidor remoto mediante este marcador.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-112">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
  
<span data-ttu-id="ba1ea-113">El ejemplo de código siguiente muestra cómo llamar a **IMAPISession::OpenMsgStore** con el indicador **MDB_ONLINE** establecido en el parámetro *ulFlags* para abrir el almacén predeterminado en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="ba1ea-113">The following code sample shows how to call **IMAPISession::OpenMsgStore** with the **MDB_ONLINE** flag set in the  *ulFlags*  parameter to open the default store on the remote server.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ba1ea-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba1ea-114">See also</span></span>

- [<span data-ttu-id="ba1ea-115">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="ba1ea-115">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="ba1ea-116">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ba1ea-116">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="ba1ea-117">Acceder a un almacén en el servidor remoto cuando Outlook está en modo caché de Exchange</span><span class="sxs-lookup"><span data-stu-id="ba1ea-117">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)


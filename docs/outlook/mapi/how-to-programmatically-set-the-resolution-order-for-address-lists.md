---
title: Establecer mediante programación el orden de resolución para las listas de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Última modificación: 06 de julio de 2012'
ms.openlocfilehash: 676d74c6441716203006f2db3e4a7d5777320a98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817000"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a><span data-ttu-id="568be-103">Establecer mediante programación el orden de resolución para las listas de direcciones</span><span class="sxs-lookup"><span data-stu-id="568be-103">Programmatically set the resolution order for address lists</span></span>
  
<span data-ttu-id="568be-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="568be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="568be-105">Este tema contiene un ejemplo de código en C++ que establece mediante programación el orden de las listas de direcciones por qué los destinatarios de correo electrónico se resuelven los mensajes y los asistentes de las convocatorias de reunión.</span><span class="sxs-lookup"><span data-stu-id="568be-105">This topic contains a code sample in C++ that programmatically sets the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span>
  
<span data-ttu-id="568be-106">En MAPI, cada perfil puede admitir varias listas de direcciones y cada lista de direcciones se encuentra en su propio contenedor.</span><span class="sxs-lookup"><span data-stu-id="568be-106">In MAPI, each profile can support multiple address lists and each address list resides in its own container.</span></span> <span data-ttu-id="568be-107">MAPI es compatible con el método **[SetSearchPath](http://support.microsoft.com/kb/292590)** en la interfaz que le permite establecer una nueva ruta de acceso de búsqueda en el perfil que se usa para la resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="568be-107">MAPI supports the **[SetSearchPath](http://support.microsoft.com/kb/292590)** method in the interface that allows you to set a new search path in the profile that is used for name resolution.</span></span> <span data-ttu-id="568be-108">Para usar el método **IAddrBook::SetSearchPath** , tiene que definir el orden de resolución deseada en una matriz de **[SRowSet](srowset.md)** que contiene los contenedores de las libretas de direcciones relevantes en el orden que desee y, a continuación, especifique la matriz como la *lpSearchPath*  parámetro.</span><span class="sxs-lookup"><span data-stu-id="568be-108">To use the **IAddrBook::SetSearchPath** method, you have to define the desired resolution order in a **[SRowSet](srowset.md)** array that holds the containers of the relevant address books in the desired order, and then specify the array as the  *lpSearchPath*  parameter.</span></span> <span data-ttu-id="568be-109">La primera propiedad para cada entrada en la matriz de **SRowSet** debe ser la propiedad de **[entrada del objeto](pidtagentryid-canonical-property.md)** de la libreta de direcciones correspondiente.</span><span class="sxs-lookup"><span data-stu-id="568be-109">The first property for each entry in the **SRowSet** array must be the **[PR_ENTRYID](pidtagentryid-canonical-property.md)** property of the corresponding address book.</span></span> 
  
<span data-ttu-id="568be-110">El ejemplo de código establece el orden de resolución de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="568be-110">The code sample sets the resolution order in the following steps:</span></span>
  
1. <span data-ttu-id="568be-111">Inicializa `numANR` para el número de contenedores para que coincida con y especifica los nombres y el orden de resolución de las listas de direcciones que desee en un `ANROrder` matriz.</span><span class="sxs-lookup"><span data-stu-id="568be-111">Initializes  `numANR` to the number of containers to match, and specifies the names and resolution order of the desired address lists in an  `ANROrder` array.</span></span> 
    
2. <span data-ttu-id="568be-112">Inicializa MAPI mediante la función **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="568be-112">Initializes MAPI by using the **MAPIInitialize** function.</span></span> 
    
3.  <span data-ttu-id="568be-113">Inicia sesión en MAPI y permite al usuario elegir un perfil.</span><span class="sxs-lookup"><span data-stu-id="568be-113">Logs on to MAPI and allows the user to choose a profile.</span></span> 
    
4.  <span data-ttu-id="568be-114">Obtiene un puntero a la libreta de direcciones de la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="568be-114">Gets a pointer to the address book from the current session.</span></span> 
    
5. <span data-ttu-id="568be-115">Se abre la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="568be-115">Opens the Address Book.</span></span>
    
6. <span data-ttu-id="568be-116">Se abre el contenedor de la raíz de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="568be-116">Opens the container for the root Address Book.</span></span>
    
7. <span data-ttu-id="568be-117">Se abre en la tabla de jerarquía del contenedor de la libreta de direcciones raíz.</span><span class="sxs-lookup"><span data-stu-id="568be-117">Opens the hierarchy table of the root address book container.</span></span>
    
8. <span data-ttu-id="568be-118">Obtiene la lista de direcciones contenedores de libretas en la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="568be-118">Gets the list of address book containers in the hierarchy.</span></span>
    
9. <span data-ttu-id="568be-119">Busca los identificadores de entrada de las listas de direcciones que desee mediante la comparación de los nombres de las listas de direcciones que desee en `ANROrder` a los nombres existentes en la jerarquía de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="568be-119">Looks for the entry IDs of the desired address lists by comparing the names of the desired address lists in  `ANROrder` to the existing names in the address book hierarchy.</span></span> 
    
10. <span data-ttu-id="568be-120">Establece los identificadores de entrada correspondiente a la matriz de **SRowSet** , `pNewRows`.</span><span class="sxs-lookup"><span data-stu-id="568be-120">Sets the appropriate entry IDs to the **SRowSet** array,  `pNewRows`.</span></span>
    
11. <span data-ttu-id="568be-121">Las llamadas y pasa `pNewRows` como el parámetro *lpSearchPath* para **IAddrBook::SetSearchPath** para establecer la ruta de acceso de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="568be-121">Calls and passes  `pNewRows` as the  *lpSearchPath*  parameter to **IAddrBook::SetSearchPath** to set the search path.</span></span> 
    
12. <span data-ttu-id="568be-122">Limpia los punteros y los búferes internos.</span><span class="sxs-lookup"><span data-stu-id="568be-122">Cleans up internal buffers and pointers.</span></span>
    
13. <span data-ttu-id="568be-123">Cierra la sesión de MAPI.</span><span class="sxs-lookup"><span data-stu-id="568be-123">Logs off from MAPI.</span></span>
    
14. <span data-ttu-id="568be-124">Uninitalizes MAPI.</span><span class="sxs-lookup"><span data-stu-id="568be-124">Uninitalizes MAPI.</span></span>
    
<span data-ttu-id="568be-125">Este ejemplo de código usa las listas de direcciones que están disponibles en la instalación predeterminada de Microsoft Office Outlook: **Todos los contactos**, **Todos los grupos**y **contactos**.</span><span class="sxs-lookup"><span data-stu-id="568be-125">This code sample uses address lists that are available in the default installation of Microsoft Office Outlook: **All Contacts**, **All Groups**, and **Contacts**.</span></span> <span data-ttu-id="568be-126">Debe ejecutar el ejemplo después de que Outlook se inicia y se está ejecutando en un perfil de inicializado.</span><span class="sxs-lookup"><span data-stu-id="568be-126">You must run the sample after Outlook is started and is running on an initialized profile.</span></span> <span data-ttu-id="568be-127">El ejemplo funciona bien con los nombres que se encuentran en un idioma (por ejemplo, todos los nombres están en inglés).</span><span class="sxs-lookup"><span data-stu-id="568be-127">The sample works well with names that are in one language (for example, all names are in English).</span></span> <span data-ttu-id="568be-128">No está diseñado para que funcionen en las implementaciones de varios idiomas, por ejemplo la carpeta de **contactos** localizada para un usuario que ejecuta una compilación que no sean - inglés de Outlook.</span><span class="sxs-lookup"><span data-stu-id="568be-128">It is not designed to work in multi-lingual deployments, for example the **Contacts** folder localized for a user running a non-English Outlook build.</span></span> 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a><span data-ttu-id="568be-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="568be-129">See also</span></span>

- [<span data-ttu-id="568be-130">Información sobre cómo establecer el orden de resolución de las listas de direcciones en Outlook</span><span class="sxs-lookup"><span data-stu-id="568be-130">About Setting the Resolution Order for Address Lists in Outlook</span></span>](about-setting-the-resolution-order-for-address-lists-in-outlook.md)


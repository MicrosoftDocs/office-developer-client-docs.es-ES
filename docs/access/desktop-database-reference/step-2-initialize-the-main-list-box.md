---
title: 'Paso 2: Inicializar el cuadro de lista principal'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485754"
---
# <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="d94c9-102">Paso 2: Inicializar el cuadro de lista principal</span><span class="sxs-lookup"><span data-stu-id="d94c9-102">Step 2: Initialize the Main List Box</span></span>


<span data-ttu-id="d94c9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d94c9-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="d94c9-104">Paso 2: Inicializar el cuadro de lista principal</span><span class="sxs-lookup"><span data-stu-id="d94c9-104">Step 2: Initialize the Main List Box</span></span>

<span data-ttu-id="d94c9-105">**Para declarar objetos Record y Recordset globales**</span><span class="sxs-lookup"><span data-stu-id="d94c9-105">**To declare global Record and Recordset objects**</span></span>

  - <span data-ttu-id="d94c9-106">Inserte el código siguiente en la sección de declaraciones generales de Form1:</span><span class="sxs-lookup"><span data-stu-id="d94c9-106">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    <span data-ttu-id="d94c9-107">Este código declara referencias de objetos globales para **Record** y **Recordset** que se usarán posteriormente en este escenario.</span><span class="sxs-lookup"><span data-stu-id="d94c9-107">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

<span data-ttu-id="d94c9-108">**Para conectar con una dirección URL y llenar lstMain**</span><span class="sxs-lookup"><span data-stu-id="d94c9-108">**To connect to a URL and populate lstMain**</span></span>

  - <span data-ttu-id="d94c9-109">Inserte el código siguiente en el controlador del evento Form Load para Form1:</span><span class="sxs-lookup"><span data-stu-id="d94c9-109">Insert the following code into the Form Load event handler for Form1:</span></span>
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    <span data-ttu-id="d94c9-110">Este código crea instancias de los objetos globales **Record** y **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="d94c9-110">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="d94c9-111">El **registro**, grec, se abre con una dirección URL especificada como **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="d94c9-111">The **Record**, grec, is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="d94c9-112">Si la dirección URL existe, se abre; si aún no existe, se crea.</span><span class="sxs-lookup"><span data-stu-id="d94c9-112">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> <span data-ttu-id="d94c9-113">Tenga en cuenta que deberá reemplazar "https://servername/foldername/" con una dirección URL válida de su entorno.</span><span class="sxs-lookup"><span data-stu-id="d94c9-113">Note that you should replace "https://servername/foldername/" with a valid URL from your environment.</span></span> <span data-ttu-id="d94c9-114">El **objeto Recordset**, grs, se abre sobre los elementos secundarios del **Record**, grec.</span><span class="sxs-lookup"><span data-stu-id="d94c9-114">The **Recordset**, grs, is opened on the children of the **Record**, grec.</span></span> <span data-ttu-id="d94c9-115">A continuación, lstMain se rellena con los nombres de archivo de los recursos publicados en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="d94c9-115">Then lstMain is populated with the file names of the resources published to the URL.</span></span>


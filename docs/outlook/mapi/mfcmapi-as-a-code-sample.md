---
title: MFCMAPI como un ejemplo de código
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356864"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="ff22b-103">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="ff22b-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="ff22b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff22b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff22b-105">El ejemplo MFCMAPI usa la API de mensajería para proporcionar acceso a los almacenes MAPI a través de una interfaz de usuario gráfica.</span><span class="sxs-lookup"><span data-stu-id="ff22b-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="ff22b-106">Después de descargar este ejemplo, puede usar los archivos de origen para examinar ejemplos de casos de uso de muchas de las interfaces y referencias de MAPI.</span><span class="sxs-lookup"><span data-stu-id="ff22b-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="ff22b-107">Para obtener más información, consulte [interfaces MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="ff22b-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff22b-108">Select</span><span class="sxs-lookup"><span data-stu-id="ff22b-108">Platforms:</span></span>  <br/> |<span data-ttu-id="ff22b-109">Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="ff22b-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="ff22b-110">Para descargar MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff22b-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="ff22b-111">En la página [MFCMAPI](https://codeplex.com/MFCMAPI) , haga clic en la pestaña **código fuente** .</span><span class="sxs-lookup"><span data-stu-id="ff22b-111">On the [MFCMAPI](https://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="ff22b-112">En protecciones **recientes**, haga clic en **Descargar** para obtener la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="ff22b-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="ff22b-113">Lea el contrato de licencia y, a \*\*\*\* continuación, haga clic en Acepto.</span><span class="sxs-lookup"><span data-stu-id="ff22b-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="ff22b-114">En el cuadro de diálogo **Descarga de archivos**, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="ff22b-115">En el cuadro de diálogo **Guardar como** , busque la carpeta en la que desea guardar los archivos de origen y, a continuación, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="ff22b-116">En el cuadro de diálogo **Descarga completada** , haga clic en **Abrir carpeta**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="ff22b-117">También puede hacer clic en **cerrar** para cerrar el cuadro de diálogo y buscar los archivos de origen comprimidos en la carpeta en la que los guardó.</span><span class="sxs-lookup"><span data-stu-id="ff22b-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="ff22b-118">Haga clic con el botón secundario en el archivo **MFCMAPI-\<version número\>. zip** y, a continuación, haga clic en **extraer todo**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="ff22b-119">En el cuadro de diálogo que aparece, haga clic en **extraer** para extraer los archivos a la carpeta que se muestra.</span><span class="sxs-lookup"><span data-stu-id="ff22b-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="ff22b-120">También puede hacer clic en **examinar** para seleccionar o crear una carpeta diferente.</span><span class="sxs-lookup"><span data-stu-id="ff22b-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="ff22b-121">Ejecute Visual Studio 2008 como administrador.</span><span class="sxs-lookup"><span data-stu-id="ff22b-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="ff22b-122">Si el equipo ejecuta Windows XP, debe iniciar sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="ff22b-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="ff22b-123">Si su equipo ejecuta Windows Vista, debe iniciar sesión como administrador y debe hacer clic con el botón secundario en el icono de Visual Studio 2008 y, a continuación, hacer clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="ff22b-124">En Visual Studio 2008, haga clic en **archivo**, elija **abrir**y, a continuación, haga clic en **proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="ff22b-125">Vaya a la ubicación en la que guardó el ejemplo, seleccione **MFCMapi. vcproj**y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="ff22b-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="ff22b-127">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ff22b-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="ff22b-128">Para usar MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="ff22b-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="ff22b-129">En **el explorador de soluciones**, expanda el proyecto **MFCMapi** y examine los archivos de los nodos **archivos de encabezado**, archivos de **recursos**y archivos de **origen** para los escenarios de programación.</span><span class="sxs-lookup"><span data-stu-id="ff22b-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="ff22b-130">Muchos temas del método de la sección [interfaces MAPI](mapi-interfaces.md) apuntan a MFCMAPI archivos de origen para ver ejemplos de programación.</span><span class="sxs-lookup"><span data-stu-id="ff22b-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="ff22b-131">Por ejemplo, en [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) , se le pide que consulte la función `CMsgStoreDlg::OnDisplayReceiveFolderTable` en el archivo MsgStoreDlg. cpp.</span><span class="sxs-lookup"><span data-stu-id="ff22b-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ff22b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff22b-132">See also</span></span>

- [<span data-ttu-id="ff22b-133">Ejemplos de MAPI (en inglés)</span><span class="sxs-lookup"><span data-stu-id="ff22b-133">MAPI Samples</span></span>](mapi-samples.md)


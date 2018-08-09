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
ms.openlocfilehash: fc92cc8deb3d12c4bc8fca4c680fd4a675b4a578
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818392"
---
# <a name="mfcmapi-as-a-code-sample"></a><span data-ttu-id="43c3a-103">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="43c3a-103">MFCMAPI as a code sample</span></span>
 
<span data-ttu-id="43c3a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="43c3a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="43c3a-105">En el ejemplo MFCMAPI usa la API de mensajería para proporcionar acceso a los almacenes MAPI a través de una interfaz gráfica de usuario.</span><span class="sxs-lookup"><span data-stu-id="43c3a-105">The MFCMAPI sample uses the Messaging API to provide access to MAPI stores through a graphical user interface.</span></span> <span data-ttu-id="43c3a-106">Después de descargar este ejemplo, puede utilizar los archivos de origen para examinar los casos de uso de ejemplo para muchas de las interfaces MAPI y referencias.</span><span class="sxs-lookup"><span data-stu-id="43c3a-106">After you download this sample, you can use the source files to examine example usage cases for many of the MAPI interfaces and references.</span></span> <span data-ttu-id="43c3a-107">Para obtener más información, vea [Interfaces de MAPI](mapi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="43c3a-107">For more information, see [MAPI Interfaces](mapi-interfaces.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43c3a-108">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="43c3a-108">Platforms:</span></span>  <br/> |<span data-ttu-id="43c3a-109">Microsoft Visual Studio 2008 para compilar para Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="43c3a-109">Microsoft Visual Studio 2008 to compile for Windows 7, Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
### <a name="to-download-mfcmapi"></a><span data-ttu-id="43c3a-110">Para descargar MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="43c3a-110">To download MFCMAPI</span></span>
  
1. <span data-ttu-id="43c3a-111">En la página [MFCMAPI](http://codeplex.com/MFCMAPI) , haga clic en la ficha de **Código fuente** .</span><span class="sxs-lookup"><span data-stu-id="43c3a-111">On the [MFCMAPI](http://codeplex.com/MFCMAPI) page, click the **Source Code** tab.</span></span> 
    
2. <span data-ttu-id="43c3a-112">**Protecciones recientes**, haga clic en **Descargar** para la compilación más reciente.</span><span class="sxs-lookup"><span data-stu-id="43c3a-112">Under **Recent Check-Ins**, click **Download** for the most recent build.</span></span> 
    
3. <span data-ttu-id="43c3a-113">Lea el contrato de licencia y, a continuación, haga clic en **acepto**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-113">Read the license agreement, and then click **I Agree**.</span></span>
    
4. <span data-ttu-id="43c3a-114">En el cuadro de diálogo **Descarga de archivos** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-114">In the **File Download** dialog box, click **Save**.</span></span> <span data-ttu-id="43c3a-115">En el cuadro de diálogo **Guardar como** , busque la carpeta en la que desea guardar los archivos de origen y, a continuación, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-115">In the **Save As** dialog box, locate the folder in which you want to save the source files, and then click **Save**.</span></span>
    
5. <span data-ttu-id="43c3a-116">En el cuadro de diálogo **Descarga completa** , haga clic en **Abrir la carpeta**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-116">In the **Download Complete** dialog box, click **Open Folder**.</span></span> <span data-ttu-id="43c3a-117">También puede hacer clic en **Cerrar** para cerrar el cuadro de diálogo y busque los archivos de origen comprimidos en la carpeta que guardó en.</span><span class="sxs-lookup"><span data-stu-id="43c3a-117">You can also click **Close** to close the dialog box and locate the zipped source files in the folder that you saved them in.</span></span> 
    
6. <span data-ttu-id="43c3a-118">Haga clic en el **MFCMAPI -\<número de versión\>.zip** de archivo y, a continuación, haga clic en **Extraer todos**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-118">Right-click the **MFCMAPI-\<version number\>.zip** file, and then click **Extract All**.</span></span> <span data-ttu-id="43c3a-119">En el cuadro de diálogo que aparece, haga clic en **extraer** para extraer los archivos a la carpeta que se muestra.</span><span class="sxs-lookup"><span data-stu-id="43c3a-119">In the dialog box that appears, click **Extract** to extract the files to the folder that is displayed.</span></span> <span data-ttu-id="43c3a-120">También puede hacer clic en **Examinar** para seleccionar o crear una carpeta diferente.</span><span class="sxs-lookup"><span data-stu-id="43c3a-120">You can also click **Browse** to select or create a different folder.</span></span> 
    
7. <span data-ttu-id="43c3a-121">Ejecute Visual Studio 2008 como administrador.</span><span class="sxs-lookup"><span data-stu-id="43c3a-121">Run Visual Studio 2008 as an administrator.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="43c3a-122">Si su equipo está ejecutando Windows XP, debe haber iniciado sesión como administrador.</span><span class="sxs-lookup"><span data-stu-id="43c3a-122">If your computer is running Windows XP, you must be logged in as an administrator.</span></span> <span data-ttu-id="43c3a-123">Si su equipo ejecuta Windows Vista, debe haber iniciado sesión como administrador y debe (ratón) en el icono de Visual Studio 2008 y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-123">If your computer is running Windows Vista, you must be logged in as an administrator and you must right-click the Visual Studio 2008 icon and then click **Run as administrator**.</span></span> 
  
8. <span data-ttu-id="43c3a-124">En Visual Studio 2008, haga clic en **archivo**, elija **Abrir**y, a continuación, haga clic en **Proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-124">In Visual Studio 2008, click **File**, point to **Open**, and then click **Project/Solution**.</span></span>
    
9. <span data-ttu-id="43c3a-125">Vaya a la ubicación donde guardó el ejemplo, seleccione **MFCMapi.vcproj**y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-125">Browse to the location where you saved the sample, select **MFCMapi.vcproj**, and then click **Open**.</span></span>
    
10. <span data-ttu-id="43c3a-126">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-126">On the **Build** menu, click **Build Solution**.</span></span>
    
11. <span data-ttu-id="43c3a-127">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="43c3a-127">In the **Save File As** dialog box, click **Save**.</span></span>
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a><span data-ttu-id="43c3a-128">Para usar MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="43c3a-128">To use MFCMAPI as a code sample</span></span>
  
<span data-ttu-id="43c3a-129">En el **Explorador de soluciones**, expanda el proyecto **MFCMapi** y examine los archivos de los nodos de **Archivos de encabezado**, **Archivos de recursos**y **Archivos de origen** para escenarios de programación.</span><span class="sxs-lookup"><span data-stu-id="43c3a-129">In **Solution Explorer**, expand the **MFCMapi** project and examine the files in the **Header Files**, **Resource Files**, and **Source Files** nodes for programming scenarios.</span></span> 
  
<span data-ttu-id="43c3a-130">Elija los archivos de origen MFCMAPI para ver ejemplos de programación temas muchos de los métodos en la sección de [Interfaces de MAPI](mapi-interfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="43c3a-130">Many method topics in the [MAPI Interfaces](mapi-interfaces.md) section point to MFCMAPI source files for programming examples.</span></span> <span data-ttu-id="43c3a-131">Por ejemplo, en [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) que se indique examine la función `CMsgStoreDlg::OnDisplayReceiveFolderTable` en el archivo MsgStoreDlg.cpp.</span><span class="sxs-lookup"><span data-stu-id="43c3a-131">For example, in [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) you are instructed to look at the function  `CMsgStoreDlg::OnDisplayReceiveFolderTable` in the MsgStoreDlg.cpp file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="43c3a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="43c3a-132">See also</span></span>

- [<span data-ttu-id="43c3a-133">Ejemplos de MAPI</span><span class="sxs-lookup"><span data-stu-id="43c3a-133">MAPI Samples</span></span>](mapi-samples.md)


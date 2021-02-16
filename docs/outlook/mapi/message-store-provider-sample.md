---
title: Ejemplo de proveedor de almacén de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436870"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="1c0ca-103">Ejemplo de proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="1c0ca-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="1c0ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c0ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c0ca-105">El proveedor de almacenamiento PST ajustado de ejemplo usa un proveedor de archivos de carpetas personales (PST) como back-end para almacenar datos.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="1c0ca-106">El proveedor del almacén de PST ajustado debe usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="1c0ca-107">La API de replicación permite replicar elementos de un repositorio de datos back-end en un almacén pst de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="1c0ca-108">Use la API de replicación para replicar los datos en un almacén de PST dedicado y realizar un seguimiento del estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="1c0ca-109">Para obtener más información, vea [Acerca de la API de replicación.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="1c0ca-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="1c0ca-110">La mayoría de las funciones del proveedor de almacenamiento pst ajustado de ejemplo pasan sus argumentos directamente al proveedor de PST subyacente.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="1c0ca-111">Algunas funciones requieren una implementación especial y se describen en los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c0ca-112">Ejecutable:</span><span class="sxs-lookup"><span data-stu-id="1c0ca-112">Executable:</span></span>  <br/> |<span data-ttu-id="1c0ca-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="1c0ca-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="1c0ca-114">Directorio de código fuente:</span><span class="sxs-lookup"><span data-stu-id="1c0ca-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="1c0ca-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="1c0ca-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="1c0ca-116">Idioma:</span><span class="sxs-lookup"><span data-stu-id="1c0ca-116">Language:</span></span>  <br/> |<span data-ttu-id="1c0ca-117">C++</span><span class="sxs-lookup"><span data-stu-id="1c0ca-117">C++</span></span>  <br/> |
|<span data-ttu-id="1c0ca-118">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="1c0ca-118">Platforms:</span></span>  <br/> |<span data-ttu-id="1c0ca-119">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="1c0ca-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="1c0ca-120">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="1c0ca-120">Supported Features</span></span>

<span data-ttu-id="1c0ca-121">Este ejemplo es compatible con Microsoft Outlook 2010 de 64 bits y ahora se ha revisado para Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="1c0ca-122">Consulte los siguientes temas para obtener información adicional:</span><span class="sxs-lookup"><span data-stu-id="1c0ca-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="1c0ca-123">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="1c0ca-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="1c0ca-124">Inicialización de un proveedor de almacén de PST ajustado</span><span class="sxs-lookup"><span data-stu-id="1c0ca-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="1c0ca-125">Inicio de sesión en un proveedor de almacén de PST ajustado</span><span class="sxs-lookup"><span data-stu-id="1c0ca-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="1c0ca-126">Uso de un proveedor de almacén de PST ajustado</span><span class="sxs-lookup"><span data-stu-id="1c0ca-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="1c0ca-127">Apagar un proveedor de almacén de PST ajustado</span><span class="sxs-lookup"><span data-stu-id="1c0ca-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="1c0ca-128">**Para instalar el proveedor de almacenamiento PST ajustado de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="1c0ca-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="1c0ca-129">Para descargar el proveedor de ARCHIVOS PST ajustados de ejemplo, consulte [Descargar los ejemplos MAPI de Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1c0ca-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="1c0ca-130">Busque la carpeta donde guardó los ejemplos MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="1c0ca-131">Haga clic con el botón secundario en la carpeta zip Número de versión **\< \> de OutlookMAPISamples** y, a continuación, haga **clic en Extraer todo**.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="1c0ca-132">Haga **clic en** Examinar, seleccione la ubicación donde desea guardar el ejemplo y, a continuación, haga clic en **Extraer**.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="1c0ca-133">Ejecute Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="1c0ca-134">En Microsoft Visual Studio 2008, haga clic en Archivo **,** seleccione **Abrir** y, a continuación, haga clic en **Proyecto/Solución.**</span><span class="sxs-lookup"><span data-stu-id="1c0ca-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="1c0ca-135">Vaya a la ubicación donde guardó el ejemplo, haga clic en **WrapPST.vcproj** y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="1c0ca-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="1c0ca-137">En el **cuadro de diálogo Guardar archivo** como, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="1c0ca-138">En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en **el archivoinstall.bat** y, a continuación, haga clic en Ejecutar como **administrador.**</span><span class="sxs-lookup"><span data-stu-id="1c0ca-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="1c0ca-139">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    


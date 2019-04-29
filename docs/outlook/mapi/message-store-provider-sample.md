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
# <a name="message-store-provider-sample"></a><span data-ttu-id="711b0-103">Ejemplo de proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="711b0-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="711b0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="711b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="711b0-105">El proveedor de almacén de archivos PST ajustado de ejemplo usa un proveedor de archivos de carpetas personales (PST) como back-end para almacenar datos.</span><span class="sxs-lookup"><span data-stu-id="711b0-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="711b0-106">El proveedor de almacén de archivos PST ajustado debe usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="711b0-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="711b0-107">La API de replicación permite replicar elementos de un repositorio de datos back-end en un almacén de archivos PST de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="711b0-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="711b0-108">La API de replicación se usa para replicar los datos en un almacén de archivos PST dedicado y realizar un seguimiento del estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="711b0-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="711b0-109">Para obtener más información, vea [acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="711b0-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="711b0-110">La mayoría de las funciones del proveedor de almacén de archivos PST ajustado de ejemplo pasan sus argumentos directamente al proveedor de PST subyacente.</span><span class="sxs-lookup"><span data-stu-id="711b0-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="711b0-111">Algunas funciones requieren una implementación especial y se describen en los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="711b0-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="711b0-112">Ejecutable</span><span class="sxs-lookup"><span data-stu-id="711b0-112">Executable:</span></span>  <br/> |<span data-ttu-id="711b0-113">WrpPST32. dll</span><span class="sxs-lookup"><span data-stu-id="711b0-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="711b0-114">Directorio de código fuente:</span><span class="sxs-lookup"><span data-stu-id="711b0-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="711b0-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="711b0-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="711b0-116">Idioma</span><span class="sxs-lookup"><span data-stu-id="711b0-116">Language:</span></span>  <br/> |<span data-ttu-id="711b0-117">+</span><span class="sxs-lookup"><span data-stu-id="711b0-117">C++</span></span>  <br/> |
|<span data-ttu-id="711b0-118">Select</span><span class="sxs-lookup"><span data-stu-id="711b0-118">Platforms:</span></span>  <br/> |<span data-ttu-id="711b0-119">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="711b0-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="711b0-120">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="711b0-120">Supported Features</span></span>

<span data-ttu-id="711b0-121">Este ejemplo admite Microsoft Outlook 2010 64-bit y ahora se ha revisado para Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="711b0-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="711b0-122">Consulte los siguientes temas para obtener más información:</span><span class="sxs-lookup"><span data-stu-id="711b0-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="711b0-123">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="711b0-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="711b0-124">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="711b0-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="711b0-125">Inicio de sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="711b0-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="711b0-126">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="711b0-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="711b0-127">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="711b0-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="711b0-128">**Para instalar el proveedor de almacén de archivos PST ajustado en muestra**</span><span class="sxs-lookup"><span data-stu-id="711b0-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="711b0-129">Para descargar el proveedor de archivos PST ajustado de muestra, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="711b0-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="711b0-130">Busque la carpeta en la que guardó los ejemplos de MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="711b0-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="711b0-131">Haga clic con el botón secundario en la carpeta ZIP del **\<\> número de versión OutlookMAPISamples** y, a continuación, haga clic en **extraer todo**.</span><span class="sxs-lookup"><span data-stu-id="711b0-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="711b0-132">Haga clic en **examinar**, seleccione la ubicación en la que desea guardar el ejemplo y, a continuación, haga clic en **extraer**.</span><span class="sxs-lookup"><span data-stu-id="711b0-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="711b0-133">Ejecute Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="711b0-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="711b0-134">En Microsoft Visual Studio 2008, haga clic en **archivo**, seleccione **abrir**y, a continuación, haga clic en **proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="711b0-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="711b0-135">Vaya a la ubicación en la que guardó el ejemplo, haga clic en **WrapPST. vcproj**y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="711b0-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="711b0-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="711b0-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="711b0-137">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="711b0-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="711b0-138">En la carpeta donde guardó el ejemplo, haga clic con el botón secundario en el archivo **install. bat** y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="711b0-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="711b0-139">En el cuadro de diálogo **Control de cuentas de usuario**, haga clic en **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="711b0-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    


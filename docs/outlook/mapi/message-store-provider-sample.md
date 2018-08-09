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
ms.openlocfilehash: b3c907b0a53a41a52516b23ffb1cf7400d887d89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818391"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="be644-103">Ejemplo de proveedor de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="be644-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="be644-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be644-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be644-105">El proveedor de almacén de archivos PST ajustado de ejemplo usa un proveedor de carpetas personales (PST) de archivo como back-end para almacenar los datos.</span><span class="sxs-lookup"><span data-stu-id="be644-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="be644-106">El proveedor de almacén de archivos PST ajustado debe usarse junto con la API de replicación.</span><span class="sxs-lookup"><span data-stu-id="be644-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="be644-107">La API de replicación permite replicar los elementos de un repositorio de datos de back-end en un almacén de archivos PST de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="be644-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="be644-108">Usar la API de replicación para replicar los datos en un almacén de archivos PST dedicado y realizar un seguimiento de estado de sincronización.</span><span class="sxs-lookup"><span data-stu-id="be644-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="be644-109">Para obtener más información, vea [Acerca de la API de replicación](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="be644-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="be644-110">La mayoría de las funciones en el proveedor de almacén de archivos PST ajustado de ejemplo pasa sus argumentos directamente al proveedor de PST subyacente.</span><span class="sxs-lookup"><span data-stu-id="be644-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="be644-111">Ciertas funciones requieren implementación especial y se describen en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="be644-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be644-112">Archivo ejecutable:</span><span class="sxs-lookup"><span data-stu-id="be644-112">Executable:</span></span>  <br/> |<span data-ttu-id="be644-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="be644-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="be644-114">Directorio de origen del código:</span><span class="sxs-lookup"><span data-stu-id="be644-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="be644-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="be644-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="be644-116">Idioma:</span><span class="sxs-lookup"><span data-stu-id="be644-116">Language:</span></span>  <br/> |<span data-ttu-id="be644-117">C++</span><span class="sxs-lookup"><span data-stu-id="be644-117">C++</span></span>  <br/> |
|<span data-ttu-id="be644-118">Plataformas:</span><span class="sxs-lookup"><span data-stu-id="be644-118">Platforms:</span></span>  <br/> |<span data-ttu-id="be644-119">Microsoft Visual Studio 2008 para compilar para Windows Vista, Windows Server 2008, Windows XP SP2 y Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="be644-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="be644-120">Características admitidas</span><span class="sxs-lookup"><span data-stu-id="be644-120">Supported Features</span></span>

<span data-ttu-id="be644-121">En este ejemplo es compatible con Microsoft Outlook 2010 de 64 bits y ahora se ha revisado para Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="be644-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="be644-122">Consulte los siguientes temas para obtener información adicional:</span><span class="sxs-lookup"><span data-stu-id="be644-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="be644-123">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="be644-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="be644-124">Inicializar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="be644-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="be644-125">Iniciar sesión en un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="be644-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="be644-126">Usar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="be644-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="be644-127">Apagar un proveedor de almacén de archivos PST ajustado</span><span class="sxs-lookup"><span data-stu-id="be644-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="be644-128">**Para instalar al proveedor de almacén de archivos PST ajustado de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="be644-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="be644-129">Para descargar el proveedor de PST ajustado de ejemplo, consulte [descargar los ejemplos de MAPI de Outlook](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="be644-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="be644-130">Busque la carpeta donde guardó los ejemplos de MAPI de Outlook.</span><span class="sxs-lookup"><span data-stu-id="be644-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="be644-131">Haga clic en el **OutlookMAPISamples -\<número de versión\> ** zip de carpeta y, a continuación, haga clic en **Extraer todos**.</span><span class="sxs-lookup"><span data-stu-id="be644-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="be644-132">Haga clic en **Examinar**, seleccione la ubicación donde desea guardar el ejemplo y, a continuación, haga clic en **extraer**.</span><span class="sxs-lookup"><span data-stu-id="be644-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="be644-133">Ejecute Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="be644-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="be644-134">En Microsoft Visual Studio 2008, haga clic en **archivo**, seleccione **Abrir**y, a continuación, haga clic en **Proyecto o solución**.</span><span class="sxs-lookup"><span data-stu-id="be644-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="be644-135">Vaya a la ubicación donde guardó el ejemplo, haga clic en **WrapPST.vcproj**y, a continuación, haga clic en **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="be644-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="be644-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="be644-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="be644-137">En el cuadro de diálogo **Guardar archivo como** , haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="be644-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="be644-138">En la carpeta donde guardó el ejemplo, haga clic en el archivo **install.bat** y, a continuación, haga clic en **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="be644-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="be644-139">En el cuadro de diálogo **Control de cuentas de usuario** , haga clic en **continuar**.</span><span class="sxs-lookup"><span data-stu-id="be644-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    


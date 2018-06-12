---
title: Compatibilidad de Office para Android con el marco de acceso de almacenamiento de Android
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cfed295-f499-44dc-bac5-9e266df1b5b3
description: Office para Android se integra con el marco de acceso de almacenamiento de Android, que permite que Office abra los archivos almacenados por otro proveedor de documentos.
ms.openlocfilehash: c217eb2aa6c0974c32e60f5015449de7b157d39d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816025"
---
# <a name="office-for-android-support-for-the-android-storage-access-framework"></a><span data-ttu-id="5791b-103">Compatibilidad de Office para Android con el marco de acceso de almacenamiento de Android</span><span class="sxs-lookup"><span data-stu-id="5791b-103">Office for Android support for the Android Storage Access Framework</span></span>

<span data-ttu-id="5791b-104">Office para Android se integra con el marco de acceso de almacenamiento de Android, que permite que Office abra los archivos almacenados por otro proveedor de documentos.</span><span class="sxs-lookup"><span data-stu-id="5791b-104">Office for Android integrates with the Android Storage Access Framework, which enables Office to open files stored by another document provider.</span></span>
  
<span data-ttu-id="5791b-p101">Android 4.4 (API nivel 19) presenta el marco de acceso de almacenamiento (SAF). El SAF permite que los usuarios busquen y abran documentos, imágenes y otros archivos en todos sus proveedores de almacenamiento de documentos preferidos. Una IU estándar permite que los usuarios busquen archivos y tengan acceso a estos de forma coherente en todos los proveedores y aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5791b-p101">Android 4.4 (API level 19) introduces the Storage Access Framework (SAF). The SAF enables users to browse and open documents, images, and other files across all their preferred document storage providers. A standard UI lets users browse files and access them in a consistent way across apps and providers.</span></span>
  
## <a name="implement-a-document-provider"></a><span data-ttu-id="5791b-108">Implementar un proveedor de documentos</span><span class="sxs-lookup"><span data-stu-id="5791b-108">Implement a document provider</span></span>

<span data-ttu-id="5791b-p102">Si está desarrollando una aplicación que proporciona servicios de almacenamiento para documentos, puede hacer que sus archivos estén disponibles a través del SAF mediante la [escritura de un proveedor de documentos personalizado](https://developer.android.com/guide/topics/providers/document-provider.html). Las aplicaciones de Office pueden invocar el propósito [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) o [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) para recibir los archivos devueltos por el proveedor de documentos. Tenga en cuenta que el propósito puede incluir filtros para ajustar más los criterios.</span><span class="sxs-lookup"><span data-stu-id="5791b-p102">If you're developing an app that provides storage services for documents, you can make your files available through the SAF by [writing a custom document provider](https://developer.android.com/guide/topics/providers/document-provider.html). Office apps can then invoke the [ACTION_OPEN_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) and/or [ACTION_CREATE_DOCUMENT](https://developer.android.com/reference/android/content/Intent.html) intent to receive the files returned by your document provider. Note that the intent might include filters to further refine the criteria.</span></span> 
  
## <a name="enable-free-consumer-edits"></a><span data-ttu-id="5791b-112">Habilitar modificaciones gratuitas para consumidores</span><span class="sxs-lookup"><span data-stu-id="5791b-112">Enable free consumer edits</span></span>

<span data-ttu-id="5791b-p103">Los usuarios pueden iniciar sesión en las aplicaciones de Office con una cuenta gratuita de Microsoft para crear o editar los documentos que se almacenan en un servicio de almacenamiento orientado al consumidor. En la siguiente tabla se enumeran las propiedades obligatorias que los proveedores deben proporcionar como parte del cursor para poder habilitar la modificación gratuita para clientes de los documentos que tienen acceso mediante el marco de acceso de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5791b-p103">Users can sign in to the Office apps with a free Microsoft account to create or edit docs that are stored in a consumer-oriented storage service. The following table lists the mandatory properties that providers must supply as part of the cursor, to enable free consumer edit for documents accessed via the Storage Access Framework.</span></span>
  
|<span data-ttu-id="5791b-115">**Propiedad**</span><span class="sxs-lookup"><span data-stu-id="5791b-115">**Property**</span></span>|<span data-ttu-id="5791b-116">**Índice**</span><span class="sxs-lookup"><span data-stu-id="5791b-116">**Index**</span></span>|<span data-ttu-id="5791b-117">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5791b-117">**Value**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5791b-118">Tipo de documento</span><span class="sxs-lookup"><span data-stu-id="5791b-118">Document Type</span></span>  <br/> |<span data-ttu-id="5791b-119">com_microsoft_office_doctype</span><span class="sxs-lookup"><span data-stu-id="5791b-119">com_microsoft_office_doctype</span></span>  <br/> |<span data-ttu-id="5791b-120">\<consumidor\></span><span class="sxs-lookup"><span data-stu-id="5791b-120">\<consumer\></span></span>  <br/> |
|<span data-ttu-id="5791b-121">Nombre descriptivo del servicio</span><span class="sxs-lookup"><span data-stu-id="5791b-121">Service Friendly Name</span></span>  <br/> |<span data-ttu-id="5791b-122">com_microsoft_office_servicename</span><span class="sxs-lookup"><span data-stu-id="5791b-122">com_microsoft_office_servicename</span></span>  <br/> |<span data-ttu-id="5791b-p104">Cualquier nombre descriptivo para el servicio, que se use para identificar un documento en la lista de elementos recientes en las aplicaciones de Office. Tenga en cuenta que se debe proporcionar la propiedad "Contrato de condiciones de uso" para que se pueda mostrar el nombre descriptivo del servicio.</span><span class="sxs-lookup"><span data-stu-id="5791b-p104">Any user-friendly name for the service, used to identify a document in the Recent list in the Office apps. Note that the "Terms of Use Agreement" property must be supplied before the friendly name for the service can be displayed.</span></span>  <br/> |
|<span data-ttu-id="5791b-125">Contrato de condiciones de uso</span><span class="sxs-lookup"><span data-stu-id="5791b-125">Terms of Use Agreement</span></span>  <br/> |<span data-ttu-id="5791b-126">com_microsoft_office_termsofuse</span><span class="sxs-lookup"><span data-stu-id="5791b-126">com_microsoft_office_termsofuse</span></span>  <br/> |<span data-ttu-id="5791b-127">\<Acepto los términos que se encuentran en http://go.microsoft.com/fwlink/p/?LinkId=528381\></span><span class="sxs-lookup"><span data-stu-id="5791b-127">\<I agree to the terms located at http://go.microsoft.com/fwlink/p/?LinkId=528381\></span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5791b-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="5791b-128">See also</span></span>
<span data-ttu-id="5791b-129"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="5791b-129"></span></span>

- [<span data-ttu-id="5791b-130">Integración con Office</span><span class="sxs-lookup"><span data-stu-id="5791b-130">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="5791b-131">Conceptos básicos sobre el proveedor de contenido</span><span class="sxs-lookup"><span data-stu-id="5791b-131">Content Provider Basics</span></span>](hhttps://developer.android.com/guide/topics/providers/content-provider-basics.html)
    
- [<span data-ttu-id="5791b-132">Creación de un proveedor de contenido</span><span class="sxs-lookup"><span data-stu-id="5791b-132">Creating a Content Provider</span></span>](https://developer.android.com/guide/topics/providers/content-provider-creating.html)
    
- [<span data-ttu-id="5791b-133">Guía para desarrolladores del marco de acceso de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="5791b-133">Storage Access Framework Developer Guide</span></span>](https://developer.android.com/guide/topics/providers/document-provider.html)
    


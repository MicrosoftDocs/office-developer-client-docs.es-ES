---
title: Propiedad canónica PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415057"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="13d45-103">Propiedad canónica PidTagReceiveFolderSettings</span><span class="sxs-lookup"><span data-stu-id="13d45-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="13d45-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13d45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13d45-105">Contiene una tabla de la configuración de la carpeta de recepción de un almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13d45-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13d45-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="13d45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13d45-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="13d45-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="13d45-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="13d45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="13d45-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="13d45-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="13d45-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="13d45-110">Data type:</span></span>  <br/> |<span data-ttu-id="13d45-111">PT OBJECT</span><span class="sxs-lookup"><span data-stu-id="13d45-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="13d45-112">Área:</span><span class="sxs-lookup"><span data-stu-id="13d45-112">Area:</span></span>  <br/> |<span data-ttu-id="13d45-113">Almacén de mensajes MAPI</span><span class="sxs-lookup"><span data-stu-id="13d45-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13d45-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13d45-114">Remarks</span></span>

<span data-ttu-id="13d45-115">Esta propiedad se puede excluir en las operaciones de [IMAPIProp:: CopyTo](imapiprop-copyto.md) o incluirse en las operaciones de [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="13d45-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="13d45-116">Como una propiedad de tipo PT Object, el método [IMAPIProp:: GetProps](imapiprop-getprops.md) no puede recuperarlo correctamente; debe obtener acceso a su contenido mediante el método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , que solicita la interfaz con el identificador IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="13d45-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="13d45-117">Los proveedores de servicios deben informar al método [IMAPIProp:: GetPropList](imapiprop-getproplist.md) si está establecido, pero, opcionalmente, puede informar de él o no si no se ha establecido.</span><span class="sxs-lookup"><span data-stu-id="13d45-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="13d45-118">Para recuperar el contenido de la tabla, una aplicación cliente debe llamar al método [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) .</span><span class="sxs-lookup"><span data-stu-id="13d45-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="13d45-119">Para obtener más información, vea [Receive Folder tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="13d45-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="13d45-120">Esta propiedad contiene una tabla de asignaciones de las carpetas de recepción del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13d45-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="13d45-121">Llamar a **OpenProperty** en esta propiedad equivale a llamar a **GetReceiveFolderTable** en el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="13d45-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="13d45-122">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="13d45-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="13d45-123">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="13d45-123">Header files</span></span>

<span data-ttu-id="13d45-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="13d45-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="13d45-125">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="13d45-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="13d45-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="13d45-126">Mapitags.h</span></span>
  
> <span data-ttu-id="13d45-127">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="13d45-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13d45-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="13d45-128">See also</span></span>



[<span data-ttu-id="13d45-129">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="13d45-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13d45-130">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="13d45-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13d45-131">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="13d45-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13d45-132">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="13d45-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


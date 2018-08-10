---
title: Propiedad canónica PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 398ff2fd4bab49c8279e198e3efa416c53abda7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819943"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a><span data-ttu-id="6ee31-103">Propiedad canónica PidTagProfileHomeServerFQDN</span><span class="sxs-lookup"><span data-stu-id="6ee31-103">PidTagProfileHomeServerFQDN Canonical Property</span></span>

  
  
<span data-ttu-id="6ee31-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ee31-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ee31-105">Habilita la autenticación Kerberos de una configuración de perfil.</span><span class="sxs-lookup"><span data-stu-id="6ee31-105">Enables Kerberos authentication of a profile configuration.</span></span>
  
****

|||
|:-----|:-----|
|<span data-ttu-id="6ee31-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="6ee31-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ee31-107">PR_PROFILE_HOME_SERVER_FQDN</span><span class="sxs-lookup"><span data-stu-id="6ee31-107">PR_PROFILE_HOME_SERVER_FQDN</span></span>  <br/> |
|<span data-ttu-id="6ee31-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6ee31-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ee31-109">0x662A001F</span><span class="sxs-lookup"><span data-stu-id="6ee31-109">0x662A001F</span></span>  <br/> |
|<span data-ttu-id="6ee31-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="6ee31-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ee31-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6ee31-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6ee31-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6ee31-112">Area:</span></span>  <br/> |<span data-ttu-id="6ee31-113">Configuración de perfiles de MAPI</span><span class="sxs-lookup"><span data-stu-id="6ee31-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ee31-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ee31-114">Remarks</span></span>

<span data-ttu-id="6ee31-115">Al establecer esta propiedad en el nombre de dominio de servidor de Active directory del usuario permite la conexión directa para el controlador de dominio (DC), que es necesario para un perfil que se ha configurado para usar la autenticación Kerberos frente a Microsoft Exchange Server 2007 y versiones anteriores, estableciendo **RPC_C_AUTHN_GSS_KERBEROS** en **PR_PROFILE_AUTH_PACKAGE**.</span><span class="sxs-lookup"><span data-stu-id="6ee31-115">Setting this property to the Domain Name of the user's directory server allows direct connection to the Domain Controller (DC), which is necessary for a profile that has been configured to use Kerberos authentication against Microsoft Exchange Server 2007 and earlier versions, by setting **RPC_C_AUTHN_GSS_KERBEROS** in **PR_PROFILE_AUTH_PACKAGE**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6ee31-116">Microsoft Exchange Server 2010 y Exchange Server 2013 controlan las llamadas de la libreta de direcciones realizadas en el servidor de acceso de cliente de forma diferente de la manera en que Exchange Server 2007 y versiones anteriores controlan.</span><span class="sxs-lookup"><span data-stu-id="6ee31-116">Microsoft Exchange Server 2010 and Exchange Server 2013 handle address book calls made to the Client Access Server differently from the way in which Exchange Server 2007 and earlier versions handle them.</span></span> <span data-ttu-id="6ee31-117">Ya no se usa el proceso DSProxy, por lo que se puede realizar correctamente la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="6ee31-117">The DSProxy process is no longer used, so Kerberos authentication may succeed.</span></span> <span data-ttu-id="6ee31-118">Sin embargo, el cliente aún podría comunicarse con el servidor de Exchange en lugar de hacerlo directamente con el controlador de dominio, es posible que no desee: configuración **PR_PROFILE_HOME_SERVER_FQDN** evita esto.</span><span class="sxs-lookup"><span data-stu-id="6ee31-118">However, the client would still be communicating with the Exchange server instead of directly with the DC, which may not be desired: Setting **PR_PROFILE_HOME_SERVER_FQDN** avoids this.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6ee31-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ee31-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6ee31-120">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="6ee31-120">Protocol specifications</span></span>

<span data-ttu-id="6ee31-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ee31-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ee31-122">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="6ee31-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6ee31-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6ee31-123">[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6ee31-124">Especifica las operaciones permitidas para los objetos de almacén de mensajes principales.</span><span class="sxs-lookup"><span data-stu-id="6ee31-124">Specifies permissible operations for the core message store objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6ee31-125">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="6ee31-125">Header files</span></span>

<span data-ttu-id="6ee31-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6ee31-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ee31-127">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="6ee31-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ee31-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6ee31-128">Mapitags.h</span></span>
  
> <span data-ttu-id="6ee31-129">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="6ee31-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ee31-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ee31-130">See also</span></span>



[<span data-ttu-id="6ee31-131">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6ee31-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ee31-132">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="6ee31-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ee31-133">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="6ee31-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ee31-134">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="6ee31-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

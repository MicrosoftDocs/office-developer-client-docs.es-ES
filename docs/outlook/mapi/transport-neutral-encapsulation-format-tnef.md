---
title: Formato de encapsulamiento neutro para el transporte (TNEF)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 98d4fe3c-3908-4cd2-bfdb-ff1874a80b24
description: 'Última modificación: 12 de marzo de 2013'
ms.openlocfilehash: d902039fa1081e30947ddd8f70ead9ae7acec06a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428693"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="7a12b-103">Formato de encapsulamiento neutro para el transporte (TNEF)</span><span class="sxs-lookup"><span data-stu-id="7a12b-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="7a12b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a12b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a12b-105">TNEF es un formato para convertir un conjunto de propiedades MAPI (un mensaje MAPI) en una secuencia de datos de serie.</span><span class="sxs-lookup"><span data-stu-id="7a12b-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="7a12b-106">Las funciones TNEF las usan principalmente los proveedores de transporte que necesitan codificar las propiedades de los mensajes MAPI para su transmisión a través de un sistema de mensajería que no admite esas propiedades directamente.</span><span class="sxs-lookup"><span data-stu-id="7a12b-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="7a12b-107">Por ejemplo, un transporte basado en SMTP usa TNEF para codificar propiedades como **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que no tienen representaciones directas en la estructura de un mensaje SMTP.</span><span class="sxs-lookup"><span data-stu-id="7a12b-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="7a12b-108">La implementación de TNEF define varios atributos específicos de TNEF, cada uno de los cuales corresponde a una propiedad MAPI determinada.</span><span class="sxs-lookup"><span data-stu-id="7a12b-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="7a12b-109">Estos atributos se usan para codificar sus respectivas propiedades MAPI en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="7a12b-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="7a12b-110">Además, se define un atributo especial que se puede usar para encapsular cualquier propiedad MAPI que no tenga un atributo específico correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7a12b-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="7a12b-111">La razón por la que se definen estos atributos, en lugar de simplemente usar un método de codificación uniforme para todas las propiedades MAPI, es habilitar la compatibilidad con versiones anteriores con software no compatible con MAPI que usa TNEF.</span><span class="sxs-lookup"><span data-stu-id="7a12b-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="7a12b-112">En el resto de esta sección se describe la estructura y la sintaxis de una secuencia TNEF, la asignación entre propiedades MAPI y atributos TNEF y consideraciones importantes para determinados atributos TNEF.</span><span class="sxs-lookup"><span data-stu-id="7a12b-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  


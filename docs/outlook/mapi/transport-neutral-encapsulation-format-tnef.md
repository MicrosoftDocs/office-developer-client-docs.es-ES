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
ms.openlocfilehash: 34b64df25cb2f7f591f7c799dec957a0072840dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820886"
---
# <a name="transport-neutral-encapsulation-format-tnef"></a><span data-ttu-id="94856-103">Formato de encapsulamiento neutro para el transporte (TNEF)</span><span class="sxs-lookup"><span data-stu-id="94856-103">Transport-Neutral Encapsulation Format (TNEF)</span></span>

 
  
<span data-ttu-id="94856-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="94856-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="94856-105">TNEF es un formato para convertir un conjunto de propiedades MAPI, un mensaje MAPI: en una secuencia de datos en serie.</span><span class="sxs-lookup"><span data-stu-id="94856-105">TNEF is a format for converting a set of MAPI properties—a MAPI message—into a serial data stream.</span></span> <span data-ttu-id="94856-106">Las funciones TNEF se usan principalmente los proveedores de transporte que necesitan para codificar las propiedades de mensaje MAPI para la transmisión a través de un sistema de mensajería que no es compatible con esas propiedades directamente.</span><span class="sxs-lookup"><span data-stu-id="94856-106">The TNEF functions are primarily used by transport providers that need to encode MAPI message properties for transmission through a messaging system that does not support those properties directly.</span></span> <span data-ttu-id="94856-107">Por ejemplo, un transporte basado en SMTP utiliza TNEF para codificar propiedades como **PR_SENT_REPRESENTING_NAME de MAPI** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), que no tienen directos representaciones en la estructura de un mensaje SMTP.</span><span class="sxs-lookup"><span data-stu-id="94856-107">For example, an SMTP-based transport uses TNEF to encode properties like **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)), which do not have direct representations in the structure of an SMTP message.</span></span>
  
<span data-ttu-id="94856-108">La implementación de TNEF define varios atributos específicos de TNEF, cada uno de los cuales corresponde a una propiedad determinada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="94856-108">The TNEF implementation defines several TNEF-specific attributes, each of which corresponds to a particular MAPI property.</span></span> <span data-ttu-id="94856-109">Estos atributos se utilizan para codificar sus respectivas propiedades MAPI en la secuencia TNEF.</span><span class="sxs-lookup"><span data-stu-id="94856-109">These attributes are used to encode their respective MAPI properties into the TNEF stream.</span></span> <span data-ttu-id="94856-110">Además, se define un atributo especial que se pueden utilizar para encapsular cualquier propiedad MAPI que no tiene un atributo específico correspondiente a ella.</span><span class="sxs-lookup"><span data-stu-id="94856-110">In addition, a special attribute is defined that can be used to encapsulate any MAPI property that does not have a specific attribute corresponding to it.</span></span> <span data-ttu-id="94856-111">La razón estos atributos están definidos, en lugar de usar simplemente una uniforme codificación para todas las propiedades MAPI (método) — es permitir la compatibilidad con versiones anteriores con el software compatible con MAPI que está utilizando la codificación TNEF.</span><span class="sxs-lookup"><span data-stu-id="94856-111">The reason these attributes are defined — instead of simply using a uniform encoding method for all MAPI properties — is to enable backward compatibility with non-MAPI-compliant software that is using TNEF.</span></span>
  
<span data-ttu-id="94856-112">En el resto de esta sección se describe la estructura y la sintaxis de una secuencia TNEF, la asignación entre las propiedades MAPI y atributos TNEF y consideraciones importantes para ciertos atributos TNEF.</span><span class="sxs-lookup"><span data-stu-id="94856-112">The remainder of this section describes the structure and syntax of a TNEF stream, the mapping between MAPI properties and TNEF attributes, and important considerations for certain TNEF attributes.</span></span>
  


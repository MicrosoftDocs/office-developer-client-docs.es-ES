---
title: Crear identificadores de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427951"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="720ca-103">Crear identificadores de entrada</span><span class="sxs-lookup"><span data-stu-id="720ca-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="720ca-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="720ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="720ca-105">Los identificadores de entrada se construyen con la [estructura ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="720ca-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="720ca-106">La **estructura ENTRYID** se compone de una marca que describe los atributos del identificador de entrada y el identificador de entrada real.</span><span class="sxs-lookup"><span data-stu-id="720ca-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="720ca-107">Estructura ENTRYID</span><span class="sxs-lookup"><span data-stu-id="720ca-107">ENTRYID Structure</span></span>

<span data-ttu-id="720ca-108">La **estructura ENTRYID** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="720ca-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="720ca-109">MAPI_DIM es una constante que se define en el archivo de encabezado MapiDefs.h.</span><span class="sxs-lookup"><span data-stu-id="720ca-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="720ca-110">El primer byte del miembro **abFlags** de 4 bytes describe el tipo y el uso del identificador de entrada y puede tener los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="720ca-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="720ca-111">MAPI_NOTRECI: indica que el identificador de entrada no se puede usar como destinatario en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="720ca-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="720ca-112">MAPI_NOTRESERVED: indica que otros usuarios no pueden tener acceso al identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="720ca-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="720ca-113">MAPI_NOW: indica que el identificador de entrada no se puede usar en otras ocasiones.</span><span class="sxs-lookup"><span data-stu-id="720ca-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="720ca-114">MAPI_SHORTTERM: indica que el identificador de entrada es a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="720ca-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="720ca-115">Todos los demás valores de este byte deben establecerse a menos que se permiten otros usos del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="720ca-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="720ca-116">MAPI_THISSESSION: indica que el identificador de entrada no se puede usar en otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="720ca-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="720ca-117">MAPI_NOTRESERVED: indica que otros proveedores de servicios pueden usar el identificador de entrada para otros objetos.</span><span class="sxs-lookup"><span data-stu-id="720ca-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="720ca-118">El **miembro ab** de los identificadores de entrada creados por los proveedores de libreta de direcciones y almacén de mensajes se compone de dos partes: una estructura [MAPIUID](mapiuid.md) de 16 bytes que identifica el proveedor de servicios y una parte para identificar el objeto.</span><span class="sxs-lookup"><span data-stu-id="720ca-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="720ca-119">**MAPIUID** es una estructura que contiene un identificador único global o GUID.</span><span class="sxs-lookup"><span data-stu-id="720ca-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="720ca-120">Un GUID es un identificador independiente del orden de bytes que se puede crear con la herramienta Microsoft Visual Studio \*Crear GUID\*\*.</span><span class="sxs-lookup"><span data-stu-id="720ca-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio *Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="720ca-121">Un proveedor de servicios registra su estructura **MAPIUID** con MAPI durante el proceso de inicio de sesión en una llamada al método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="720ca-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="720ca-122">Cuando un cliente llama a un **método OpenEntry** para obtener acceso a un objeto, MAPI usa la estructura **MAPIUID** para determinar qué proveedor de servicios puede proporcionar ese acceso.</span><span class="sxs-lookup"><span data-stu-id="720ca-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="720ca-123">Los proveedores de servicios deben usar la misma **estructura MAPIUID** para todas las versiones de su DLL.</span><span class="sxs-lookup"><span data-stu-id="720ca-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="720ca-124">Esto permite a los clientes con la versión más reciente responder a los mensajes enviados y guardados con la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="720ca-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="720ca-125">El resto del **miembro ab** después del **MAPIUID** de 16 bytes contiene datos binarios específicos del proveedor de servicios para identificar objetos concretos.</span><span class="sxs-lookup"><span data-stu-id="720ca-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="720ca-126">No hay un tamaño fijo para esta parte del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="720ca-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="720ca-127">Puede ser de cualquier tamaño, dentro de la razón.</span><span class="sxs-lookup"><span data-stu-id="720ca-127">It can be any size, within reason.</span></span> <span data-ttu-id="720ca-128">Normalmente, un proveedor de servicios incluye la siguiente información en esta parte de sus identificadores de entrada:</span><span class="sxs-lookup"><span data-stu-id="720ca-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="720ca-129">Información de versión: dado que es habitual que un proveedor de servicios cambie el formato de sus identificadores de entrada de una versión a otra, el almacenamiento de información de versión permite determinar rápidamente cómo descifrar cualquier identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="720ca-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="720ca-130">Información de ubicación: la información de ubicación son datos que dan a un proveedor de servicios un indicador de cómo localizar el objeto representado por el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="720ca-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="720ca-131">Por ejemplo, un proveedor de servicios puede almacenar el desplazamiento del disco para el último lugar en un archivo de datos en el que se ha almacenado el objeto.</span><span class="sxs-lookup"><span data-stu-id="720ca-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="720ca-132">Dado que este tipo de información puede cambiar con el tiempo, los proveedores de servicios deben proporcionar varias formas de buscar objetos en sus identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="720ca-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="720ca-133">Aunque los proveedores de servicios pueden reciclar sus identificadores de entrada, deben evitar esta práctica.</span><span class="sxs-lookup"><span data-stu-id="720ca-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="720ca-134">Si es necesario volver a usar un identificador de entrada, los proveedores de servicios deben hacer que el período de tiempo que transcurra entre el uso inicial y la reutilización siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="720ca-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="720ca-135">Además, el identificador de entrada debe reasignarse a otro objeto del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="720ca-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="720ca-136">Es decir, un identificador de entrada determinado no debe asociarse primero con un mensaje y, a continuación, con una carpeta.</span><span class="sxs-lookup"><span data-stu-id="720ca-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="720ca-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="720ca-137">See also</span></span>



[<span data-ttu-id="720ca-138">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="720ca-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)


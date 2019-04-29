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
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="c8298-103">Crear identificadores de entrada</span><span class="sxs-lookup"><span data-stu-id="c8298-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="c8298-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8298-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8298-105">Los identificadores de entrada se construyen con la estructura [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="c8298-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="c8298-106">La estructura **EntryID** está compuesta por una marca que describe los atributos del identificador de entrada y el identificador de entrada real.</span><span class="sxs-lookup"><span data-stu-id="c8298-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="c8298-107">Estructura ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c8298-107">ENTRYID Structure</span></span>

<span data-ttu-id="c8298-108">La estructura **EntryID** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="c8298-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="c8298-109">MAPI_DIM es una constante que se define en el archivo de encabezado MapiDefs. h.</span><span class="sxs-lookup"><span data-stu-id="c8298-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="c8298-110">El primer byte del miembro **abFlags** de 4 bytes describe el tipo y uso del identificador de entrada y puede tener los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8298-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="c8298-111">MAPI_NOTRECI: indica que el identificador de entrada no se puede usar como un destinatario en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="c8298-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="c8298-112">MAPI_NOTRESERVED: indica que otros usuarios no pueden tener acceso al identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8298-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="c8298-113">MAPI_NOW: indica que el identificador de entrada no se puede usar en otros momentos.</span><span class="sxs-lookup"><span data-stu-id="c8298-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="c8298-114">MAPI_SHORTTERM: indica que el identificador de entrada es a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="c8298-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="c8298-115">Se deben establecer todos los demás valores de este byte, a menos que se permitan otros usos del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8298-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="c8298-116">MAPI_THISSESSION: indica que el identificador de entrada no se puede usar en otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="c8298-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="c8298-117">MAPI_NOTRESERVED: indica que otros proveedores de servicios pueden usar el identificador de entrada para otros objetos.</span><span class="sxs-lookup"><span data-stu-id="c8298-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="c8298-118">El miembro **AB** de los identificadores de entrada que crea la libreta de direcciones y los proveedores de almacenamiento de mensajes consta de dos partes: una estructura [MAPIUID](mapiuid.md) de 16 bytes que identifica al proveedor de servicios y una parte para identificar el objeto.</span><span class="sxs-lookup"><span data-stu-id="c8298-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="c8298-119">**MAPIUID** es una estructura que contiene un identificador único global (GUID).</span><span class="sxs-lookup"><span data-stu-id="c8298-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="c8298-120">Un GUID es un identificador independiente de orden de bytes que se puede crear mediante la herramienta Microsoft Visual Studio\*Create GUID\*\*.</span><span class="sxs-lookup"><span data-stu-id="c8298-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="c8298-121">Un proveedor de servicios registra su estructura **MAPIUID** con MAPI durante el proceso de inicio de sesión en una llamada al método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) .</span><span class="sxs-lookup"><span data-stu-id="c8298-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="c8298-122">Cuando un cliente llama a un método **OpenEntry** para tener acceso a un objeto, MAPI usa la estructura **MAPIUID** para determinar qué proveedor de servicios puede proporcionar ese acceso.</span><span class="sxs-lookup"><span data-stu-id="c8298-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="c8298-123">Los proveedores de servicios deben usar la misma estructura **MAPIUID** para todas las versiones de su dll.</span><span class="sxs-lookup"><span data-stu-id="c8298-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="c8298-124">Esto permite que los clientes con la versión más reciente respondan a los mensajes enviados y guardados con la versión anterior.</span><span class="sxs-lookup"><span data-stu-id="c8298-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="c8298-125">El resto del miembro **AB** después del **MAPIUID** de 16 bytes contiene datos binarios específicos del proveedor de servicios para identificar objetos determinados.</span><span class="sxs-lookup"><span data-stu-id="c8298-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="c8298-126">No hay ningún tamaño fijo para esta parte del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8298-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="c8298-127">Puede tener cualquier tamaño, en razón.</span><span class="sxs-lookup"><span data-stu-id="c8298-127">It can be any size, within reason.</span></span> <span data-ttu-id="c8298-128">Un proveedor de servicios suele incluir la siguiente información en esta parte de sus identificadores de entrada:</span><span class="sxs-lookup"><span data-stu-id="c8298-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="c8298-129">Información de la versión: debido a que es habitual que un proveedor de servicios cambie el formato de sus identificadores de entrada de una versión a otra, el almacenamiento de la información de versión permite determinar rápidamente cómo descifrar cualquier identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8298-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="c8298-130">Información de Ubicación: la información de ubicación es un dato que proporciona a un proveedor de servicios un indicador de cómo localizar el objeto representado por el identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8298-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="c8298-131">Por ejemplo, un proveedor de servicios puede almacenar el desplazamiento de disco para la última posición en un archivo de datos que se almacenó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c8298-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="c8298-132">Debido a que este tipo de información puede cambiar con el tiempo, los proveedores de servicios deben proporcionar varias formas de localizar los objetos en sus identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="c8298-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="c8298-133">Aunque los proveedores de servicios pueden reciclar sus identificadores de entrada, deben evitar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c8298-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="c8298-134">Si es necesario reutilizar un identificador de entrada, los proveedores de servicios deben realizar el período de tiempo que transcurre entre el uso inicial y la reutilización siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="c8298-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="c8298-135">Además, el identificador de entrada debe reasignarse a otro objeto del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="c8298-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="c8298-136">Es decir, un identificador de entrada determinado no debe asociarse primero con un mensaje y luego con una carpeta.</span><span class="sxs-lookup"><span data-stu-id="c8298-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8298-137">Ver también</span><span class="sxs-lookup"><span data-stu-id="c8298-137">See also</span></span>



[<span data-ttu-id="c8298-138">Identificadores de entrada MAPI</span><span class="sxs-lookup"><span data-stu-id="c8298-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)


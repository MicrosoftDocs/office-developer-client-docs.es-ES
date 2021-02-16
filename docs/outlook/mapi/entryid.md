---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415274"
---
# <a name="entryid"></a><span data-ttu-id="fab71-103">ENTRYID</span><span class="sxs-lookup"><span data-stu-id="fab71-103">ENTRYID</span></span>

  
  
<span data-ttu-id="fab71-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fab71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fab71-105">Contiene un identificador de entrada para un objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="fab71-105">Contains an entry identifier for a MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fab71-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fab71-106">Header file:</span></span>  <br/> |<span data-ttu-id="fab71-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fab71-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fab71-108">Macros relacionadas:</span><span class="sxs-lookup"><span data-stu-id="fab71-108">Related macros:</span></span>  <br/> |<span data-ttu-id="fab71-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span><span class="sxs-lookup"><span data-stu-id="fab71-109">[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a><span data-ttu-id="fab71-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fab71-110">Members</span></span>

 <span data-ttu-id="fab71-111">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="fab71-111">**abFlags**</span></span>
  
> <span data-ttu-id="fab71-112">Máscara de bits de marcas que proporcionan información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="fab71-112">Bitmask of flags that provide information that describes the object.</span></span> <span data-ttu-id="fab71-113">Solo el proveedor puede establecer el primer byte de las marcas, **abFlags[0];** las otras tres están reservadas.</span><span class="sxs-lookup"><span data-stu-id="fab71-113">Only the first byte of the flags, **abFlags[0]**, may be set by the provider; the other three are reserved.</span></span> <span data-ttu-id="fab71-114">Estas marcas no deben establecerse para identificadores de entrada permanentes; solo se establecen para identificadores de entrada a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="fab71-114">These flags must not be set for permanent entry identifiers; they are only set for short-term entry identifiers.</span></span> <span data-ttu-id="fab71-115">Para los clientes, esta estructura es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fab71-115">To clients, this structure is read-only.</span></span> <span data-ttu-id="fab71-116">Las siguientes marcas se pueden establecer en **abFlags[0]**:</span><span class="sxs-lookup"><span data-stu-id="fab71-116">The following flags can be set in **abFlags[0]**:</span></span>
    
<span data-ttu-id="fab71-117">MAPI_NOTRECIP</span><span class="sxs-lookup"><span data-stu-id="fab71-117">MAPI_NOTRECIP</span></span> 
  
> <span data-ttu-id="fab71-118">El identificador de entrada no se puede usar como destinatario en un mensaje.</span><span class="sxs-lookup"><span data-stu-id="fab71-118">The entry identifier cannot be used as a recipient on a message.</span></span>
    
<span data-ttu-id="fab71-119">MAPI_NOTRESERVED</span><span class="sxs-lookup"><span data-stu-id="fab71-119">MAPI_NOTRESERVED</span></span> 
  
> <span data-ttu-id="fab71-120">Otros usuarios no pueden tener acceso al identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fab71-120">Other users cannot access the entry identifier.</span></span>
    
<span data-ttu-id="fab71-121">MAPI_NOW</span><span class="sxs-lookup"><span data-stu-id="fab71-121">MAPI_NOW</span></span> 
  
> <span data-ttu-id="fab71-122">El identificador de entrada no se puede usar en otras ocasiones.</span><span class="sxs-lookup"><span data-stu-id="fab71-122">The entry identifier cannot be used at other times.</span></span>
    
<span data-ttu-id="fab71-123">MAPI_SHORTTERM</span><span class="sxs-lookup"><span data-stu-id="fab71-123">MAPI_SHORTTERM</span></span> 
  
> <span data-ttu-id="fab71-124">El identificador de entrada es a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="fab71-124">The entry identifier is short-term.</span></span> <span data-ttu-id="fab71-125">Todos los demás valores de este byte deben establecerse a menos que se habiliten otros usos del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fab71-125">All other values in this byte must be set unless other uses of the entry identifier are enabled.</span></span>
    
<span data-ttu-id="fab71-126">MAPI_THISSESSION</span><span class="sxs-lookup"><span data-stu-id="fab71-126">MAPI_THISSESSION</span></span> 
  
> <span data-ttu-id="fab71-127">El identificador de entrada no se puede usar en otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="fab71-127">The entry identifier cannot be used on other sessions.</span></span>
    
 <span data-ttu-id="fab71-128">**ab**</span><span class="sxs-lookup"><span data-stu-id="fab71-128">**ab**</span></span>
  
> <span data-ttu-id="fab71-129">Indica una matriz de datos binarios que usan los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="fab71-129">Indicates an array of binary data that is used by service providers.</span></span> <span data-ttu-id="fab71-130">La aplicación cliente no puede usar esta matriz.</span><span class="sxs-lookup"><span data-stu-id="fab71-130">The client application cannot use this array.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fab71-131">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fab71-131">Remarks</span></span>

<span data-ttu-id="fab71-132">Los **proveedores de libretas** de direcciones y el almacén de mensajes usan la estructura ENTRYID para crear identificadores únicos para sus objetos.</span><span class="sxs-lookup"><span data-stu-id="fab71-132">The **ENTRYID** structure is used by message store and address book providers to construct unique identifiers for their objects.</span></span> <span data-ttu-id="fab71-133">Los identificadores de entrada se usan para identificar los siguientes tipos de objetos:</span><span class="sxs-lookup"><span data-stu-id="fab71-133">Entry identifiers are used to identify the following types of objects:</span></span> 
  
- <span data-ttu-id="fab71-134">Almacenes de mensajes</span><span class="sxs-lookup"><span data-stu-id="fab71-134">Message stores</span></span>
    
- <span data-ttu-id="fab71-135">Folders</span><span class="sxs-lookup"><span data-stu-id="fab71-135">Folders</span></span>
    
- <span data-ttu-id="fab71-136">Mensajes</span><span class="sxs-lookup"><span data-stu-id="fab71-136">Messages</span></span>
    
- <span data-ttu-id="fab71-137">Contenedores de libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="fab71-137">Address book containers</span></span>
    
- <span data-ttu-id="fab71-138">Listas de distribución</span><span class="sxs-lookup"><span data-stu-id="fab71-138">Distribution lists</span></span>
    
- <span data-ttu-id="fab71-139">Usuarios de mensajería</span><span class="sxs-lookup"><span data-stu-id="fab71-139">Messaging users</span></span>
    
- <span data-ttu-id="fab71-140">Objetos de estado</span><span class="sxs-lookup"><span data-stu-id="fab71-140">Status objects</span></span>
    
- <span data-ttu-id="fab71-141">Secciones de perfil</span><span class="sxs-lookup"><span data-stu-id="fab71-141">Profile sections</span></span>
    
<span data-ttu-id="fab71-142">Cada proveedor usa un formato para la **estructura ENTRYID** que tiene sentido para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="fab71-142">Each provider uses a format for the **ENTRYID** structure that makes sense for that provider.</span></span> 
  
<span data-ttu-id="fab71-143">Los identificadores de entrada no pueden compararse directamente porque un objeto puede estar representado por dos valores binarios distintos.</span><span class="sxs-lookup"><span data-stu-id="fab71-143">Entry identifiers cannot be compared directly because one object can be represented by two different binary values.</span></span> <span data-ttu-id="fab71-144">Para determinar si dos identificadores de entrada representan el mismo objeto, llame al método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) .</span><span class="sxs-lookup"><span data-stu-id="fab71-144">To determine whether two entry identifiers represent the same object, call the [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) method.</span></span> 
  
<span data-ttu-id="fab71-145">Cuando un cliente llama al método [IMAPIProp::GetProps](imapiprop-getprops.md) de un objeto para recuperar su identificador de entrada, el objeto devuelve la forma más permanente del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fab71-145">When a client calls an object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its entry identifier, the object returns the most permanent form of the entry identifier.</span></span> <span data-ttu-id="fab71-146">Un cliente puede comprobar que un identificador de entrada es a largo plazo comprobando que ninguna de las marcas está establecida en el primer byte del **miembro abFlags.**</span><span class="sxs-lookup"><span data-stu-id="fab71-146">A client can verify that an entry identifier is long-term by checking that none of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="fab71-147">Cuando un cliente tiene acceso a un identificador de entrada a través de una columna de una tabla, lo más probable es que este identificador de entrada sea a corto plazo en lugar de a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="fab71-147">When a client accesses an entry identifier through a column in a table, most likely this entry identifier is short-term instead of long-term.</span></span> <span data-ttu-id="fab71-148">Los identificadores de entrada a corto plazo se pueden usar para abrir sus objetos correspondientes solo en la sesión MAPI actual.</span><span class="sxs-lookup"><span data-stu-id="fab71-148">Short-term entry identifiers can be used to open their corresponding objects only in the current MAPI session.</span></span> <span data-ttu-id="fab71-149">Un cliente puede comprobar que un identificador de entrada es a corto plazo comprobando que todas las marcas están establecidas en el primer byte del **miembro abFlags.**</span><span class="sxs-lookup"><span data-stu-id="fab71-149">A client can verify that an entry identifier is short-term by checking that all of the flags are set in the first byte of the **abFlags** member.</span></span> 
  
<span data-ttu-id="fab71-150">Algunos identificadores de entrada son a corto plazo, pero tienen un uso a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="fab71-150">Some entry identifiers are short-term, but have long-term use.</span></span> <span data-ttu-id="fab71-151">Este identificador de entrada tendrá uno o varios de los indicadores adecuados establecidos en el primer byte de su **miembro abFlags.**</span><span class="sxs-lookup"><span data-stu-id="fab71-151">Such an entry identifier will have one or more of the appropriate flags set in the first byte of its **abFlags** member.</span></span> 
  
<span data-ttu-id="fab71-152">Una **estructura ENTRYID** es similar a una [estructura FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="fab71-152">An **ENTRYID** structure resembles a [FLATENTRY](flatentry.md) structure.</span></span> <span data-ttu-id="fab71-153">Sin embargo, hay algunas diferencias:</span><span class="sxs-lookup"><span data-stu-id="fab71-153">However, there are some differences:</span></span> 
  
- <span data-ttu-id="fab71-154">Una **estructura ENTRYID** no almacena el tamaño del identificador de entrada; una **estructura FLATENTRY** sí.</span><span class="sxs-lookup"><span data-stu-id="fab71-154">An **ENTRYID** structure does not store the size of the entry identifier; a **FLATENTRY** structure does.</span></span> 
    
- <span data-ttu-id="fab71-155">Una **estructura ENTRYID** almacena los datos de marca y el resto del identificador de entrada por separado; Una **estructura FLATENTRY** almacena los datos de marca con el resto del identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="fab71-155">An **ENTRYID** structure stores the flag data and the rest of the entry identifier separately; a **FLATENTRY** structure stores the flag data with the rest of the entry identifier.</span></span> 
    
- <span data-ttu-id="fab71-156">Una estructura **ENTRYID** se pasa como parámetro a los métodos de la interfaz [IMAPIProp](imapipropiunknown.md) y a los siguientes métodos **OpenEntry:** [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="fab71-156">An **ENTRYID** structure is passed as a parameter to the methods of the [IMAPIProp](imapipropiunknown.md) interface and to the following **OpenEntry** methods: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)</span></span>
    
- <span data-ttu-id="fab71-157">Una **estructura ENTRYID** se usa para almacenar un identificador de entrada en el disco.</span><span class="sxs-lookup"><span data-stu-id="fab71-157">An **ENTRYID** structure is used to store an entry identifier on disk.</span></span> <span data-ttu-id="fab71-158">Una **estructura FLATENTRY** se usa para almacenar un identificador de entrada en un archivo o pasarlo en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="fab71-158">A **FLATENTRY** structure is used to store an entry identifier in a file or pass it in a stream of bytes.</span></span> 
    
<span data-ttu-id="fab71-159">Los clientes siempre deben pasar identificadores de entrada alineados de forma natural.</span><span class="sxs-lookup"><span data-stu-id="fab71-159">Clients should always pass in naturally aligned entry identifiers.</span></span> <span data-ttu-id="fab71-160">Aunque los proveedores deben controlar identificadores de entrada alineados arbitrariamente, los clientes no deben esperar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="fab71-160">Although providers should handle arbitrarily aligned entry identifiers, clients should not expect this behavior.</span></span> <span data-ttu-id="fab71-161">Si no se pasa un buen identificador de entrada alineado a un método, se puede producir un error de alineación en los procesadores RISC.</span><span class="sxs-lookup"><span data-stu-id="fab71-161">Failure to pass a good aligned entry identifier to a method can cause an alignment fault on RISC processors.</span></span> 
  
<span data-ttu-id="fab71-162">El factor de alineación natural, normalmente 8 bytes, es el tipo de datos más grande admitido por la CPU y normalmente el mismo factor de alineación usado por el asignador de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="fab71-162">The natural alignment factor, typically 8 bytes, is the largest data type supported by the CPU, and usually the same alignment factor used by the system memory allocator.</span></span> <span data-ttu-id="fab71-163">Una dirección de memoria alineada de forma natural permite que la CPU acceda a cualquier tipo de datos que admita en esa dirección sin generar un error de alineación.</span><span class="sxs-lookup"><span data-stu-id="fab71-163">A naturally aligned memory address allows the CPU to access any data type it supports at that address without generating an alignment fault.</span></span> <span data-ttu-id="fab71-164">Para las CPU RISC, un tipo de datos de tamaño N bytes normalmente debe alinearse en un par múltiplo de N bytes, siendo la dirección un múltiplo par de N.</span><span class="sxs-lookup"><span data-stu-id="fab71-164">For RISC CPUs, a data type of size N bytes must usually be aligned on an even multiple of N bytes, with the address being an even multiple of N.</span></span>
  
<span data-ttu-id="fab71-165">Para obtener más información, vea [Identificadores de entrada](mapi-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="fab71-165">For more information, see [Entry Identifiers](mapi-entry-identifiers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fab71-166">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fab71-166">See also</span></span>



[<span data-ttu-id="fab71-167">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="fab71-167">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="fab71-168">IMAPISupport::CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="fab71-168">IMAPISupport::CompareEntryIDs</span></span>](imapisupport-compareentryids.md)
  
[<span data-ttu-id="fab71-169">Propiedad canónica PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="fab71-169">PidTagRecordKey Canonical Property</span></span>](pidtagrecordkey-canonical-property.md)


[<span data-ttu-id="fab71-170">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="fab71-170">MAPI Structures</span></span>](mapi-structures.md)


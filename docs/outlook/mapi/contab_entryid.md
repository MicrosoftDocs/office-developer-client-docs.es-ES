---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2c8661f24ed9555547446cf63fc08a3be7e6e941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816567"
---
# <a name="contabentryid"></a><span data-ttu-id="abc8e-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="abc8e-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="abc8e-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="abc8e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="abc8e-105">Contiene el identificador de entrada de la carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="abc8e-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="abc8e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="abc8e-106">Header file:</span></span>  <br/> |<span data-ttu-id="abc8e-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="abc8e-107">msomapiutil.h</span></span>  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a><span data-ttu-id="abc8e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="abc8e-108">Members</span></span>

 <span data-ttu-id="abc8e-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="abc8e-109">**abFlags**</span></span>
  
> <span data-ttu-id="abc8e-110">Una máscara de bits de indicadores que proporciona información que describe el objeto.</span><span class="sxs-lookup"><span data-stu-id="abc8e-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="abc8e-111">Para obtener más información, vea la descripción del campo **abFlags** de una estructura de [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="abc8e-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="abc8e-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="abc8e-112">**muid**</span></span>
  
> <span data-ttu-id="abc8e-113">GUID que identifica el proveedor de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="abc8e-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="abc8e-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="abc8e-114">**ulVersion**</span></span>
  
> <span data-ttu-id="abc8e-115">El número de versión de la estructura **CONTAB_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="abc8e-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="abc8e-116">Debe establecerse en CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="abc8e-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="abc8e-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="abc8e-117">**ulType**</span></span>
  
> <span data-ttu-id="abc8e-118">Un entero que representa el tipo de identificador de entrada del contacto.</span><span class="sxs-lookup"><span data-stu-id="abc8e-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="abc8e-119">Debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="abc8e-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="abc8e-120">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="abc8e-120">**Name**</span></span>|<span data-ttu-id="abc8e-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abc8e-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="abc8e-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="abc8e-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="abc8e-123">Un objeto de usuario de mensajer�a.</span><span class="sxs-lookup"><span data-stu-id="abc8e-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="abc8e-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="abc8e-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="abc8e-125">Un objeto de lista de distribuci�n.</span><span class="sxs-lookup"><span data-stu-id="abc8e-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="abc8e-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="abc8e-126">**ulIndex**</span></span>
  
> <span data-ttu-id="abc8e-127">El índice en el subconjunto de la propiedad de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="abc8e-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="abc8e-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="abc8e-128">**cbeid**</span></span>
  
> <span data-ttu-id="abc8e-129">El tamaño del identificador de entrada del mensaje contacto asociado con esta entrada de la libreta de direcciones de contactos.</span><span class="sxs-lookup"><span data-stu-id="abc8e-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="abc8e-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="abc8e-130">**abeid**</span></span>
  
> <span data-ttu-id="abc8e-131">El identificador de entrada del mensaje contacto asociado con esta entrada de la libreta de direcciones de contactos.</span><span class="sxs-lookup"><span data-stu-id="abc8e-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="abc8e-132">Notas</span><span class="sxs-lookup"><span data-stu-id="abc8e-132">Remarks</span></span>

<span data-ttu-id="abc8e-133">Una libreta de direcciones de contactos es una libreta de direcciones que contiene todos los elementos de contacto en una carpeta de contactos que tienen una dirección de correo electrónico o un número de fax.</span><span class="sxs-lookup"><span data-stu-id="abc8e-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="abc8e-134">Cada entrada de una libreta de direcciones de contactos está asociado con una dirección de correo electrónico o un número de fax.</span><span class="sxs-lookup"><span data-stu-id="abc8e-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="abc8e-135">Dado que un elemento de contacto puede tener hasta tres direcciones de correo electrónico y tres números de fax, se puede representar un elemento de contacto por hasta seis entradas en la libreta de direcciones de los contactos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="abc8e-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="abc8e-136">El propósito de una libreta de direcciones de contactos es admitir los usuarios hacer frente a los mensajes de correo electrónico a los contactos en una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="abc8e-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="abc8e-137">El proveedor de la libreta de direcciones de contactos compatibles con Microsoft Outlook 2010 y Microsoft Outlook 2013 es contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="abc8e-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="abc8e-138">La estructura **CONTAB_ENTRYID** admite un subconjunto de la información que está presente en el mensaje de contacto de MAPI subyacente.</span><span class="sxs-lookup"><span data-stu-id="abc8e-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="abc8e-139">Identifica el mensaje de contacto que está asociada una entrada de la libreta de direcciones de contactos determinada.</span><span class="sxs-lookup"><span data-stu-id="abc8e-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="abc8e-140">Los campos **cbeid** y **abeid** sólo son válidos cuando se establece el valor del campo **ulType** en CONTAB_DISTLIST o CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="abc8e-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="abc8e-141">Cuando se establece el valor del campo **ulType** en CONTAB_ROOT, CONTAB_SUBROOT o CONTAB_CONTAINER, la estructura [DIR_ENTRYID](dir_entryid.md) debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="abc8e-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="abc8e-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="abc8e-142">See also</span></span>



[<span data-ttu-id="abc8e-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="abc8e-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="abc8e-144">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="abc8e-144">MAPI Structures</span></span>](mapi-structures.md)


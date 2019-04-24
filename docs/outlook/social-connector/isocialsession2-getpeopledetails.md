---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Devuelve una cadena que contiene una colección de personas y detalles de la imagen para los usuarios especificados por el parámetro personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344873"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="af6e7-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="af6e7-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="af6e7-104">Devuelve una cadena que contiene una colección de personas y detalles de la imagen para los usuarios especificados por el parámetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="af6e7-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="af6e7-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="af6e7-105">Parameters</span></span>

<span data-ttu-id="af6e7-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="af6e7-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="af6e7-107">a Una cadena XML que especifica las direcciones SMTP con hash de un conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="af6e7-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="af6e7-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="af6e7-108">_personsCollection_</span></span>
  
> <span data-ttu-id="af6e7-109">contempla Una cadena XML que contiene una colección de personas e información de la imagen.</span><span class="sxs-lookup"><span data-stu-id="af6e7-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af6e7-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af6e7-110">Remarks</span></span>

<span data-ttu-id="af6e7-111">Outlook Social Connector (OSC) llama a **GetPeopleDetails** si el proveedor OSC admite la sincronización a petición o híbrida de amigos y no amigos.</span><span class="sxs-lookup"><span data-stu-id="af6e7-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="af6e7-112">El parámetro _personsAddresses_ debe cumplir con la definición de esquema de **hashedAddresses**, como se define en el esquema de la extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="af6e7-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="af6e7-113">La cadena _personsAddresses_ representa un conjunto de direcciones SMTP con hash para cada usuario que se muestra en el panel de personas.</span><span class="sxs-lookup"><span data-stu-id="af6e7-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="af6e7-114">El usuario no tiene por qué ser un amigo del usuario que ha iniciado sesión representado por la propiedad [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="af6e7-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="af6e7-115">Las direcciones SMTP con hash se cifran mediante la función de hash especificada por el elemento **hashFunction** en el XML de **capacidades** del proveedor.</span><span class="sxs-lookup"><span data-stu-id="af6e7-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="af6e7-116">El OSC identifica cada **hashedAddress** de la colección _personAddresses_ con un elemento **index** .</span><span class="sxs-lookup"><span data-stu-id="af6e7-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="af6e7-117">El proveedor debe usar el elemento **index** para identificar el XML de la **persona** del destinatario cuando devuelve XML de **amigos** para **GetPeopleDetails**.</span><span class="sxs-lookup"><span data-stu-id="af6e7-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="af6e7-118">Si el destinatario no es un usuario registrado en la red social, el proveedor no debe devolver ningún XML de **persona** para ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="af6e7-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="af6e7-119">El elemento **index** para cada usuario de red representado por **Person** XML corresponde al elemento **index** del destinatario de _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="af6e7-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="af6e7-120">El OSC almacena la información devuelta por el parámetro _personsCollection_ en la memoria.</span><span class="sxs-lookup"><span data-stu-id="af6e7-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="af6e7-121">La cadena XML _personsCollection_ debe cumplir con la definición de esquema para **amigos**, tal como se define en el esquema de la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="af6e7-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="af6e7-122">Para obtener más información acerca de cómo el OSC usa y actualiza esta información en la memoria, consulte [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="af6e7-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af6e7-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="af6e7-123">See also</span></span>

- [<span data-ttu-id="af6e7-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="af6e7-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="af6e7-125">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="af6e7-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)


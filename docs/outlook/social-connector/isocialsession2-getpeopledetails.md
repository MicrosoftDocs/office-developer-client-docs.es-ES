---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Devuelve una cadena que contiene una colección de detalles de persona e imagen para los usuarios especificados por el parámetro personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404536"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="ae2f0-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="ae2f0-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="ae2f0-104">Devuelve una cadena que contiene una colección de detalles de persona e imagen para los usuarios especificados por el _parámetro personsAddresses._</span><span class="sxs-lookup"><span data-stu-id="ae2f0-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="ae2f0-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae2f0-105">Parameters</span></span>

<span data-ttu-id="ae2f0-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="ae2f0-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="ae2f0-107">[entrada] Cadena XML que especifica las direcciones SMTP con hash de un conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="ae2f0-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="ae2f0-108">_personsCollection_</span></span>
  
> <span data-ttu-id="ae2f0-109">[salida] Una cadena XML que contiene una colección de detalles de persona e imagen.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae2f0-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae2f0-110">Remarks</span></span>

<span data-ttu-id="ae2f0-111">Outlook Social Connector (OSC) llama a **GetPeopleDetails** si el proveedor de OSC admite la sincronización a petición o híbrida de amigos y no amigos.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="ae2f0-112">El  _parámetro personsAddresses_ debe cumplir con la definición de esquema para **hashedAddresses**, tal como se define en el esquema para la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="ae2f0-113">La  _cadena personsAddresses_ representa un conjunto de direcciones SMTP con hash para cada usuario que se muestra en el panel de personas.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="ae2f0-114">El usuario no tiene que ser un amigo del usuario que ha iniciado sesión representado por la propiedad [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="ae2f0-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="ae2f0-115">Las direcciones SMTP con hash se cifran mediante la función hash especificada por el elemento **hashFunction** en el XML de **capacidades del** proveedor.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="ae2f0-116">El OSC identifica cada **hashedAddress en** la  _colección personAddresses_ con un **elemento de** índice.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="ae2f0-117">El proveedor debe usar el **elemento de índice** para identificar el XML de persona del destinatario cuando devuelve el XML de amigos para **GetPeopleDetails**.  </span><span class="sxs-lookup"><span data-stu-id="ae2f0-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="ae2f0-118">Si el destinatario no es un usuario registrado en la red social, el proveedor no debe devolver ningún **XML** de persona para ese destinatario.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="ae2f0-119">El **elemento de** índice de cada usuario de red representado por xml de persona corresponde al elemento **de** índice del destinatario en _personsAddresses_. </span><span class="sxs-lookup"><span data-stu-id="ae2f0-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="ae2f0-120">El OSC almacena la información devuelta por el  _parámetro personsCollection_ en la memoria.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="ae2f0-121">La cadena XML  _personsCollection_ debe cumplir con la definición de esquema para **amigos,** tal como se define en el esquema para la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="ae2f0-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="ae2f0-122">Para obtener más información sobre cómo el OSC usa y actualiza esta información en la memoria, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="ae2f0-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae2f0-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ae2f0-123">See also</span></span>

- [<span data-ttu-id="ae2f0-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae2f0-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="ae2f0-125">Sincronizar amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="ae2f0-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)


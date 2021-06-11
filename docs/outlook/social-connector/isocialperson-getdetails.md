---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtiene una cadena que representa los detalles de la persona, como el nombre, el apellido y una dirección URL de una imagen de perfil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427335"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="0a144-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="0a144-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="0a144-104">Obtiene una cadena que representa los detalles de la persona, como el nombre, el apellido y una dirección URL de una imagen de perfil.</span><span class="sxs-lookup"><span data-stu-id="0a144-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="0a144-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="0a144-105">Parameters</span></span>

<span data-ttu-id="0a144-106">_details_</span><span class="sxs-lookup"><span data-stu-id="0a144-106">_details_</span></span>
  
> <span data-ttu-id="0a144-107">[salida] Valor de cadena XML que representa los detalles de una persona.</span><span class="sxs-lookup"><span data-stu-id="0a144-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a144-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a144-108">Remarks</span></span>

<span data-ttu-id="0a144-109">La _cadena_ XML de detalles devueltos debe cumplir con la definición de esquema para persona **,** tal como se define en el esquema para la extensibilidad del proveedor Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="0a144-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="0a144-110">El OSC llama **a GetDetails** si el proveedor de OSC admite la sincronización híbrida o en caché de amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="0a144-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="0a144-111">Cuando el OSC obtiene inicialmente las actividades de los amigos para el usuario que ha iniciado sesión, llama a [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)y almacena la información de los amigos en una carpeta de contactos específica de la red social, en el almacén de Outlook predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="0a144-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="0a144-112">Posteriormente, el OSC no llama a **GetFriendsAndColleagues** o **GetDetails** a menos que el intervalo de actualización de la memoria caché haya expirado.</span><span class="sxs-lookup"><span data-stu-id="0a144-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="0a144-113">Para obtener más información acerca de cómo el OSC almacena en caché la información de los amigos en una carpeta de contactos, vea [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="0a144-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a144-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a144-114">See also</span></span>

- [<span data-ttu-id="0a144-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a144-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)


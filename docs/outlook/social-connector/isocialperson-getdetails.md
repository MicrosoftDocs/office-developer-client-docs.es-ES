---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtiene una cadena que representa los detalles de la persona, como el nombre, apellidos y una dirección URL a una imagen de perfil.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821093"
---
# <a name="isocialpersongetdetails"></a><span data-ttu-id="f4920-103">ISocialPerson::GetDetails</span><span class="sxs-lookup"><span data-stu-id="f4920-103">ISocialPerson::GetDetails</span></span>

<span data-ttu-id="f4920-104">Obtiene una cadena que representa los detalles de la persona, como el nombre, apellidos y una dirección URL a una imagen de perfil.</span><span class="sxs-lookup"><span data-stu-id="f4920-104">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span> 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a><span data-ttu-id="f4920-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4920-105">Parameters</span></span>

<span data-ttu-id="f4920-106">_detalles_</span><span class="sxs-lookup"><span data-stu-id="f4920-106">_details_</span></span>
  
> <span data-ttu-id="f4920-107">[out] Un valor de cadena XML que representa los detalles de una persona.</span><span class="sxs-lookup"><span data-stu-id="f4920-107">[out] An XML string value that represents the details for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f4920-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4920-108">Remarks</span></span>

<span data-ttu-id="f4920-109">La cadena XML devuelto _Detalles_ debe cumplir con la definición del esquema para la **persona**, tal como se define en el esquema para la extensibilidad de proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="f4920-109">The returned  _details_ XML string must comply with the schema definition for **person**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span>
  
<span data-ttu-id="f4920-110">Las llamadas de OSC **GetDetails** si el proveedor OSC es compatible con caché o sincronización híbrido de amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4920-110">The OSC calls **GetDetails** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="f4920-111">Cuando el OSC inicialmente Obtiene las actividades de amigos para que el usuario ha iniciado la sesión, llama a [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)y almacena información de amigos en una carpeta de contactos específica a la red social, en el almacén de Outlook predeterminado del usuario conectado .</span><span class="sxs-lookup"><span data-stu-id="f4920-111">When the OSC initially gets friends' activities for the logged on user, it calls [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), and stores friends' information in a contacts folder specific to the social network, in the logged on user's default Outlook store.</span></span> <span data-ttu-id="f4920-112">Posteriormente el OSC no llama a **GetFriendsAndColleagues** o **GetDetails** a menos que el intervalo de actualización de la memoria caché ha expirado.</span><span class="sxs-lookup"><span data-stu-id="f4920-112">Subsequently the OSC does not call **GetFriendsAndColleagues** or **GetDetails** unless the refresh interval for the cache has expired.</span></span> <span data-ttu-id="f4920-113">Para obtener más información acerca de cómo el OSC recopila información de amigos en una carpeta de contactos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="f4920-113">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4920-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4920-114">See also</span></span>

- [<span data-ttu-id="f4920-115">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f4920-115">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)


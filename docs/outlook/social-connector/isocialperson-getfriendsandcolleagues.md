---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtiene una cadena que representa una colección de personas.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407658"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="4dae5-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="4dae5-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="4dae5-104">Obtiene una cadena que representa una colección de personas.</span><span class="sxs-lookup"><span data-stu-id="4dae5-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="4dae5-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4dae5-105">Parameters</span></span>

<span data-ttu-id="4dae5-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="4dae5-106">_personsCollection_</span></span>
  
> <span data-ttu-id="4dae5-107">[salida] Cadena XML que representa un conjunto de amigos de la persona  y que cumple con la definición de amigos definida en el esquema XML para la extensibilidad del proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="4dae5-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="4dae5-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4dae5-108">Remarks</span></span>

<span data-ttu-id="4dae5-109">El OSC llama a **GetFriendsAndColleagues** si el proveedor de OSC admite la sincronización híbrida o en caché de amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="4dae5-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="4dae5-110">Cuando el OSC llama inicialmente al método **GetFriendsAndColleagues** para el usuario de Outlook que ha iniciado sesión en la red social, **GetFriendsAndColleagues** devuelve una cadena XML que representa a los amigos del usuario que ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="4dae5-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="4dae5-111">La cadena XML cumple con la definición del esquema **XML** de amigos y especifica un elemento **person** (que también cumple con la definición de esquema del proveedor de OSC) para cada amigo.</span><span class="sxs-lookup"><span data-stu-id="4dae5-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="4dae5-112">Cuando **GetFriendsAndColleagues** devuelve la información de amigos del usuario que ha iniciado sesión, el OSC almacena esa información en una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="4dae5-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="4dae5-113">Esta carpeta es específica de la red social y reside en el almacén de Outlook predeterminado del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4dae5-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="4dae5-114">Para obtener más información sobre cómo el OSC almacena en caché la información de los amigos en una carpeta de contactos, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="4dae5-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="4dae5-115">La información de cada amigo devuelto en el  _parámetro personsCollection_ cumple con la definición del esquema XML para **la persona**.</span><span class="sxs-lookup"><span data-stu-id="4dae5-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="4dae5-116">El elemento **person** admite muchas partes de información para cada amigo, incluidas las direcciones de correo electrónico SMTP (que se asignan a los elementos **emailAddress**, **emailAddress2** y **emailAddress3)** que el amigo ha especificado en la red social, y el identificador de usuario (que se asigna al elemento **userID)** que identifica a ese amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="4dae5-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="4dae5-117">Para mostrar actividades para un usuario de Outlook seleccionado en el panel de personas, el OSC intenta hacer coincidir al usuario con cada amigo devuelto de **GetFriendsAndColleagues**.</span><span class="sxs-lookup"><span data-stu-id="4dae5-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="4dae5-118">Para ello, el OSC hace coincidir la dirección SMTP del usuario de Outlook seleccionado con las direcciones de correo electrónico que cada amigo ha especificado en la red social.</span><span class="sxs-lookup"><span data-stu-id="4dae5-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="4dae5-119">Si el OSC encuentra una dirección de correo electrónico SMTP que coincida, el OSC usa el **userID** correspondiente del amigo para llamar al método [ISocialSession::GetPerson.](isocialsession-getperson.md)</span><span class="sxs-lookup"><span data-stu-id="4dae5-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="4dae5-120">Lo hace para obtener un objeto [ISocialPerson](isocialpersoniunknown.md) para ese amigo, lo que permite al OSC obtener actividades e imágenes de ese amigo de la red social.</span><span class="sxs-lookup"><span data-stu-id="4dae5-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="4dae5-121">Sin embargo, si el usuario de Outlook seleccionado no especifica esa misma dirección SMTP en una cuenta de la red social, o si el usuario de Outlook no tiene una cuenta en esa red social, el OSC no podrá encontrar una coincidencia para ese usuario y no mostrará ninguna actividad para ese usuario en la red social.</span><span class="sxs-lookup"><span data-stu-id="4dae5-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4dae5-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4dae5-122">See also</span></span>

- [<span data-ttu-id="4dae5-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4dae5-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="4dae5-124">Obtener información de amigos</span><span class="sxs-lookup"><span data-stu-id="4dae5-124">Getting Friends Information</span></span>](getting-friends-information.md)


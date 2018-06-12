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
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821102"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="46fd6-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="46fd6-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="46fd6-104">Obtiene una cadena que representa una colección de personas.</span><span class="sxs-lookup"><span data-stu-id="46fd6-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="46fd6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46fd6-105">Parameters</span></span>

<span data-ttu-id="46fd6-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="46fd6-106">_personsCollection_</span></span>
  
> <span data-ttu-id="46fd6-107">[out] Una cadena XML que representa un conjunto de amigos de la persona, y que cumple con la definición de **amigos** , tal como se define en el esquema XML de extensibilidad de proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="46fd6-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="46fd6-108">Notas</span><span class="sxs-lookup"><span data-stu-id="46fd6-108">Remarks</span></span>

<span data-ttu-id="46fd6-109">Las llamadas de OSC **GetFriendsAndColleagues** si el proveedor OSC es compatible con caché o sincronización híbrido de amigos en la red social.</span><span class="sxs-lookup"><span data-stu-id="46fd6-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="46fd6-110">Cuando el OSC llama inicialmente al método **GetFriendsAndColleagues** para el usuario de Outlook que ha iniciado sesión en la red social, **GetFriendsAndColleagues** devuelve una cadena XML que representa los amigos del usuario ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="46fd6-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="46fd6-111">La cadena XML cumple con la definición de esquema XML de **amigos** y especifica un elemento **person** (que también se ajusta a la definición de esquema de proveedor OSC) para cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="46fd6-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="46fd6-112">Cuando **GetFriendsAndColleagues** devuelve los amigos información para el usuario ha iniciado sesión, el OSC almacena esa información en una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="46fd6-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="46fd6-113">Esta carpeta es específica de la red social y reside en el almacén de Outlook predeterminado del usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="46fd6-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="46fd6-114">Para obtener más información acerca de cómo el OSC recopila información de amigos en una carpeta de contactos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="46fd6-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="46fd6-115">Información de cada amigo devuelto en el parámetro _personsCollection_ cumple con la definición del esquema XML para la **persona**.</span><span class="sxs-lookup"><span data-stu-id="46fd6-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="46fd6-116">El elemento **person** admite muchos elementos de información para cada uno de ellos, incluidas las direcciones de correo electrónico SMTP (que se asignan a los elementos **emailAddress**, **emailAddress2**y **emailAddress3** ) que se ha especificado el amigo en el redes sociales y el identificador de usuario (que se asigna al elemento **userID** ) que identifica ese amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="46fd6-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="46fd6-117">Para mostrar las actividades de un usuario de Outlook seleccionado en el panel de personas, el OSC intenta hacer coincidir el usuario con cada amigo devuelto desde **GetFriendsAndColleagues**.</span><span class="sxs-lookup"><span data-stu-id="46fd6-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="46fd6-118">Para ello, el OSC que coincida con la dirección SMTP del usuario de Outlook seleccionado con las direcciones de correo electrónico que ha especificado cada uno de ellos en la red social.</span><span class="sxs-lookup"><span data-stu-id="46fd6-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="46fd6-119">Si el OSC encuentra una dirección de correo electrónico SMTP coincidente, el OSC usa el correspondiente **userID** del amigo para llamar al método [ISocialSession::GetPerson](isocialsession-getperson.md) .</span><span class="sxs-lookup"><span data-stu-id="46fd6-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="46fd6-120">Hace esto para obtener un objeto [ISocialPerson](isocialpersoniunknown.md) para ese amigo, que luego se habilita el OSC obtener las imágenes de ese amigo y actividades de la red social.</span><span class="sxs-lookup"><span data-stu-id="46fd6-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="46fd6-121">Sin embargo, si el usuario de Outlook seleccionado no especifica esa misma dirección SMTP en una cuenta en la red social, o si el usuario de Outlook no tienen una cuenta en esa red social, el OSC no será capaz de encontrar a una coincidencia para que el usuario y no mostrará ningún activiti es de dicho usuario en la red social.</span><span class="sxs-lookup"><span data-stu-id="46fd6-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="46fd6-122">Ver también</span><span class="sxs-lookup"><span data-stu-id="46fd6-122">See also</span></span>

- [<span data-ttu-id="46fd6-123">ISocialPerson: IUnknown</span><span class="sxs-lookup"><span data-stu-id="46fd6-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="46fd6-124">Obtener información sobre amigos</span><span class="sxs-lookup"><span data-stu-id="46fd6-124">Getting Friends Information</span></span>](getting-friends-information.md)


---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtiene una cadena que representa una colección de las actividades de cada uno de los usuarios especificados por el parámetro hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821129"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="f3bbd-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="f3bbd-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="f3bbd-104">Obtiene una cadena que representa una colección de las actividades de cada uno de los usuarios especificados por el parámetro _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="f3bbd-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="f3bbd-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3bbd-105">Parameters</span></span>

<span data-ttu-id="f3bbd-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="f3bbd-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="f3bbd-107">[entrada] Una estructura que especifica una matriz de SMTP con algoritmo hash de direcciones para un conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="f3bbd-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="f3bbd-108">_startTime_</span></span>
  
> <span data-ttu-id="f3bbd-109">[entrada] El tiempo tras el que se devolverán las actividades que se crean.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="f3bbd-110">_actividades_</span><span class="sxs-lookup"><span data-stu-id="f3bbd-110">_activities_</span></span>
  
> <span data-ttu-id="f3bbd-111">[out] Una cadena XML que representa el conjunto de actividades de los usuarios especificados por _hashedAddresses_ en la red social con respecto a la _hora de inicio_.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3bbd-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f3bbd-112">Remarks</span></span>

<span data-ttu-id="f3bbd-113">El OSC llama a **GetActivitiesEx** si el proveedor de OSC admite la sincronización de petición de actividades.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="f3bbd-114">El OSC almacena la información devuelta en _las actividades_ en la memoria.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="f3bbd-115">Para obtener más información acerca de cómo el OSC usa y actualiza esta información en la memoria, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="f3bbd-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="f3bbd-116">A partir de Outlook Social Connector 2013, el OSC admite la sincronización de sólo a petición de actividades y llamadas sólo **GetActivitiesEx** para obtener las actividades.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="f3bbd-117">Para admitir la búsqueda de actividades a petición, establezca **cacheActivities** como **false**y **getActivities** y **dynamicActivitiesLookupEx** como **true**y el OSC llamará **GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="f3bbd-118">La cadena XML devuelta debe cumplir con la definición del esquema para **activityFeed**, tal como se define en el esquema para la extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="f3bbd-119">El sring _hashedAddresses_ representa un conjunto de direcciones con algoritmo hash para cada usuario que se muestra en el panel de personas.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="f3bbd-120">Las direcciones SMTP con algoritmo hash se cifran mediante el uso de la función hash especificada por el elemento **hashFunction** en XML de las **capacidades del proveedor** .</span><span class="sxs-lookup"><span data-stu-id="f3bbd-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="f3bbd-121">El usuario no tiene como friend del usuario ha iniciado la sesión representado por la propiedad [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) .</span><span class="sxs-lookup"><span data-stu-id="f3bbd-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="f3bbd-122">El parámetro _startTime_ es un valor de **fecha** en hora Universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="f3bbd-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f3bbd-123">Los valores de hora local deben convertirse en los valores de **fecha** de UTC.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="f3bbd-124">Las actividades que devuelve el método **GetActivitiesEx** deben tener un valor de hora de creación que sea mayor que _startTime_ y menor o igual que **ahora**.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="f3bbd-125">Si no ha habido cambios entre **startTime** y **ahora**, el proveedor debe devolver un error OSC_E_NO_CHANGES.</span><span class="sxs-lookup"><span data-stu-id="f3bbd-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f3bbd-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3bbd-126">See also</span></span>

- [<span data-ttu-id="f3bbd-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f3bbd-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="f3bbd-128">Sincronización de amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="f3bbd-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)


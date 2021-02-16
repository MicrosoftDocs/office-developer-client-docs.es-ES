---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtiene una cadena que representa una colección de actividades de cada uno de los usuarios especificados por el parámetro hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404340"
---
# <a name="isocialsession2getactivitiesex"></a><span data-ttu-id="e2058-103">ISocialSession2::GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="e2058-103">ISocialSession2::GetActivitiesEx</span></span>

<span data-ttu-id="e2058-104">Obtiene una cadena que representa una colección de actividades de cada uno de los usuarios especificados por el _parámetro hashedAddresses._</span><span class="sxs-lookup"><span data-stu-id="e2058-104">Gets a string that represents a collection of activities of each of the users specified by the  _hashedAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a><span data-ttu-id="e2058-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2058-105">Parameters</span></span>

<span data-ttu-id="e2058-106">_hashedAddresses_</span><span class="sxs-lookup"><span data-stu-id="e2058-106">_hashedAddresses_</span></span>
  
> <span data-ttu-id="e2058-107">[entrada] Estructura que especifica una matriz de direcciones SMTP con hash para un conjunto de usuarios.</span><span class="sxs-lookup"><span data-stu-id="e2058-107">[in] A structure that specifies an array of hashed SMTP addresses for a set of users.</span></span>
    
<span data-ttu-id="e2058-108">_startTime_</span><span class="sxs-lookup"><span data-stu-id="e2058-108">_startTime_</span></span>
  
> <span data-ttu-id="e2058-109">[entrada] Tiempo después del cual se devolverán las actividades que se crearán.</span><span class="sxs-lookup"><span data-stu-id="e2058-109">[in] The time after which activities that are created would be returned.</span></span>
    
<span data-ttu-id="e2058-110">_activities_</span><span class="sxs-lookup"><span data-stu-id="e2058-110">_activities_</span></span>
  
> <span data-ttu-id="e2058-111">[salida] Una cadena XML que representa el conjunto de actividades de los usuarios especificado por  _hashedAddresses_ en la red social desde  _startTime_.</span><span class="sxs-lookup"><span data-stu-id="e2058-111">[out] An XML string that represents the set of activities of the users specified by  _hashedAddresses_ on the social network since  _startTime_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2058-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e2058-112">Remarks</span></span>

<span data-ttu-id="e2058-113">El OSC llama **a GetActivitiesEx** si el proveedor de OSC admite la sincronización a petición de las actividades.</span><span class="sxs-lookup"><span data-stu-id="e2058-113">The OSC calls **GetActivitiesEx** if the OSC provider supports on-demand synchronization of activities.</span></span> <span data-ttu-id="e2058-114">El OSC almacena la información devuelta en  _las actividades_ en la memoria.</span><span class="sxs-lookup"><span data-stu-id="e2058-114">The OSC stores the information returned in  _activities_ in memory.</span></span> <span data-ttu-id="e2058-115">Para obtener más información sobre cómo el OSC usa y actualiza esta información en la memoria, consulta Sincronizar amigos [y actividades.](synchronizing-friends-and-activities.md)</span><span class="sxs-lookup"><span data-stu-id="e2058-115">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="e2058-116">A partir de Outlook Social Connector 2013, el OSC solo admite la sincronización a petición de actividades y solo llama a **GetActivitiesEx** para obtener actividades.</span><span class="sxs-lookup"><span data-stu-id="e2058-116">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and calls only **GetActivitiesEx** to get activities.</span></span> <span data-ttu-id="e2058-117">Para admitir la búsqueda de actividades a petición, establezca **cacheActivities** como **false** y **getActivities** y **dynamicActivitiesLookupEx** como **true** y el OSC llamará **a GetActivitiesEx**.</span><span class="sxs-lookup"><span data-stu-id="e2058-117">To support on-demand activities lookup, set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, and the OSC will call **GetActivitiesEx**.</span></span>
  
<span data-ttu-id="e2058-118">La cadena XML devuelta debe cumplir con la definición de esquema de **activityFeed**, tal como se define en el esquema para la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="e2058-118">The returned XML string must comply with the schema definition for **activityFeed**, as defined in the schema for OSC provider extensibility.</span></span>
  
<span data-ttu-id="e2058-119">El  _sring hashedAddresses_ representa un conjunto de direcciones hash para cada usuario que se muestra en el panel de personas.</span><span class="sxs-lookup"><span data-stu-id="e2058-119">The  _hashedAddresses_ sring represents a set of hashed addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="e2058-120">Las direcciones SMTP con hash se cifran mediante la función hash especificada por el elemento **hashFunction** en el XML de **capacidades del** proveedor.</span><span class="sxs-lookup"><span data-stu-id="e2058-120">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="e2058-121">El usuario no tiene que ser un amigo del usuario que ha iniciado sesión representado por la propiedad [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md)</span><span class="sxs-lookup"><span data-stu-id="e2058-121">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> 
  
<span data-ttu-id="e2058-122">El  _parámetro startTime_ es un **valor de fecha** en hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="e2058-122">The  _startTime_ parameter is a **Date** value in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e2058-123">Los valores de hora local deben convertirse a valores **de fecha** UTC.</span><span class="sxs-lookup"><span data-stu-id="e2058-123">Local time values must be converted to UTC **Date** values.</span></span> 
  
<span data-ttu-id="e2058-124">Las actividades que devuelve el método **GetActivitiesEx** deben tener un valor de hora de creación mayor que  _startTime_ y menor o igual que **Now**.</span><span class="sxs-lookup"><span data-stu-id="e2058-124">Activities that the **GetActivitiesEx** method returns must have a creation time value that is greater than  _startTime_ and less than or equal to **Now**.</span></span> <span data-ttu-id="e2058-125">Si no se han producido cambios entre **startTime** y **Now**, el proveedor debe devolver OSC_E_NO_CHANGES error.</span><span class="sxs-lookup"><span data-stu-id="e2058-125">If no changes have occurred between **startTime** and **Now**, the provider must return an OSC_E_NO_CHANGES error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2058-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e2058-126">See also</span></span>

- [<span data-ttu-id="e2058-127">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2058-127">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="e2058-128">Sincronizar amigos y actividades</span><span class="sxs-lookup"><span data-stu-id="e2058-128">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)


---
title: Ejemplo XML de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: El ejemplo de XML de este tema es una cadena XML de amigo devuelta a Outlook Social Connector (OSC) después de que llama al método ISocialPerson::GetFriendsAndColleagues. En el ejemplo se muestra el XML de amigos para dos amigos, que cada uno delimitado por el elemento person. Cada uno de ellos especifica un valor único para el elemento de identificador de usuario en la red social.
ms.openlocfilehash: 5dbda1e4439f807ccc6e7abddd0ef654ae801fe0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395213"
---
# <a name="friends-xml-example"></a><span data-ttu-id="ba9da-105">Ejemplo XML de amigos</span><span class="sxs-lookup"><span data-stu-id="ba9da-105">Friends XML example</span></span>

<span data-ttu-id="ba9da-106">El ejemplo de XML de este tema es una cadena XML de amigo devuelta a Outlook Social Connector (OSC) después de que llama al método [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) .</span><span class="sxs-lookup"><span data-stu-id="ba9da-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="ba9da-107">El ejemplo muestra el XML **amigos** para dos amigos, que cada uno delimitado por el elemento de la **persona** .</span><span class="sxs-lookup"><span data-stu-id="ba9da-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="ba9da-108">Cada uno de ellos especifica un valor único para el elemento de **identificador de usuario** en la red social.</span><span class="sxs-lookup"><span data-stu-id="ba9da-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="ba9da-109">Los elementos restantes de **amigos** XML tienen nombres explican por sí solos.</span><span class="sxs-lookup"><span data-stu-id="ba9da-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="ba9da-110">Para una descripción detallada de estos elementos, vea [XML para amigos](xml-for-friends.md).</span><span class="sxs-lookup"><span data-stu-id="ba9da-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="ba9da-111">Ejemplo de XML</span><span class="sxs-lookup"><span data-stu-id="ba9da-111">XML example</span></span>

<span data-ttu-id="ba9da-112">En el ejemplo siguiente se muestra el XML **amigos** para dos personas en la red social.</span><span class="sxs-lookup"><span data-stu-id="ba9da-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <person>
    <userID>4667647</userID>
    <firstName>Melissa</firstName>
    <lastName>MacBeth</lastName>
    <nickname></nickname>
    <fileAs>MacBeth, Melissa (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Product Manager</title>
    <anniversary>2005-05-17</anniversary>
    <birthday>1979-08-09</birthday>
    <emailAddress>melissa@contoso.com</emailAddress>
    <emailAddress2>melissa@fabrikam.com</emailAddress2>
    <emailAddress3>melissa@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/melissa</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>female</gender>
    <index>0</index>
  </person>
  <person>
    <userID>5015012</userID>
    <firstName>Michael</firstName>
    <lastName>Affronti</lastName>
    <nickname>Mr. Social</nickname>
    <fileAs>Affronti, Michael (Contoso Ltd.)</fileAs>
    <company>Contoso Ltd.</company>
    <title>Sales Director</title>
    <anniversary>2009-06-21</anniversary>
    <birthday>1980-09-10</birthday>
    <emailAddress>michael@contoso.com</emailAddress>
    <emailAddress2>michael@fabrikam.com</emailAddress2>
    <emailAddress3>michael@adventureworks.com</emailAddress3>
    <webProfilePage>https://contoso.com/michael</webProfilePage>
    <phone>800-555-1212</phone>
    <cell>888-555-1212</cell>
    <workPhone>425-555-1212</workPhone>
    <creationTime>2010-01-08T08:30:20-08:00</creationTime>
    <lastModificationTime>2010-01-08T11:40:14-08:00</lastModificationTime>
    <expirationTime>2010-01-09T11:40:14-08:00</expirationTime>
    <gender>male</gender>
    <index>1</index>
  </person>
</friends>

```

## <a name="see-also"></a><span data-ttu-id="ba9da-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba9da-113">See also</span></span>

- [<span data-ttu-id="ba9da-114">Ejemplos XML de proveedor OSC</span><span class="sxs-lookup"><span data-stu-id="ba9da-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="ba9da-115">Ejemplo de XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="ba9da-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="ba9da-116">Ejemplo de XML de fuentes de actividades</span><span class="sxs-lookup"><span data-stu-id="ba9da-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="ba9da-117">Esquema XML de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="ba9da-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)


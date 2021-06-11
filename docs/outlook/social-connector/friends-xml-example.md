---
title: Ejemplo XML de amigos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83afbdef-4f12-4673-a0c1-bbf86274558f
description: El ejemplo XML de este tema es una cadena XML de amigo devuelta al conector social (OSC) de Outlook después de llamar al método ISocialPerson::GetFriendsAndColleagues. En el ejemplo se muestra el XML de amigos para dos amigos, cada uno delimitado por el elemento person. Cada amigo especifica un valor único para el elemento userID en la red social.
ms.openlocfilehash: 593019ec4dcd1b9b578bfe275fb8e6664bbd11a9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542229"
---
# <a name="friends-xml-example"></a><span data-ttu-id="bdd02-105">Ejemplo XML de amigos</span><span class="sxs-lookup"><span data-stu-id="bdd02-105">Friends XML example</span></span>

<span data-ttu-id="bdd02-106">El ejemplo XML de este tema es una cadena XML de amigos devuelta al conector social (OSC) de Outlook después de llamar al método [ISocialPerson::GetFriendsAndColleagues.](isocialperson-getfriendsandcolleagues.md)</span><span class="sxs-lookup"><span data-stu-id="bdd02-106">The XML example in this topic is a friend XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) method.</span></span> <span data-ttu-id="bdd02-107">En el ejemplo se muestra el XML **de** amigos para dos amigos, cada uno delimitado por el **elemento person.**</span><span class="sxs-lookup"><span data-stu-id="bdd02-107">The example shows the **friends** XML for two friends, each delimited by the **person** element.</span></span> <span data-ttu-id="bdd02-108">Cada amigo especifica un valor único para el **elemento userID** en la red social.</span><span class="sxs-lookup"><span data-stu-id="bdd02-108">Each friend specifies a unique value for the **userID** element on the social network.</span></span> 
  
<span data-ttu-id="bdd02-109">Los elementos restantes del XML **de amigos** tienen nombres autoexplicativos.</span><span class="sxs-lookup"><span data-stu-id="bdd02-109">The remaining elements of the **friends** XML have self-explanatory names.</span></span> <span data-ttu-id="bdd02-110">Para obtener una descripción detallada de estos elementos, vea [XML for Friends](xml-for-friends.md).</span><span class="sxs-lookup"><span data-stu-id="bdd02-110">For detailed description of these elements, see [XML for Friends](xml-for-friends.md).</span></span> 
  
## <a name="xml-example"></a><span data-ttu-id="bdd02-111">Ejemplo XML</span><span class="sxs-lookup"><span data-stu-id="bdd02-111">XML example</span></span>

<span data-ttu-id="bdd02-112">En el ejemplo siguiente se muestra el XML **de amigos** para dos personas en la red social.</span><span class="sxs-lookup"><span data-stu-id="bdd02-112">The following example shows the **friends** XML for two persons on the social network.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<friends xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

## <a name="see-also"></a><span data-ttu-id="bdd02-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdd02-113">See also</span></span>

- [<span data-ttu-id="bdd02-114">Ejemplos XML del proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="bdd02-114">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="bdd02-115">Ejemplo XML de funcionalidades</span><span class="sxs-lookup"><span data-stu-id="bdd02-115">Capabilities XML Example</span></span>](capabilities-xml-example.md) 
- [<span data-ttu-id="bdd02-116">Ejemplo XML de fuente de actividad</span><span class="sxs-lookup"><span data-stu-id="bdd02-116">Activity Feed XML Example</span></span>](activity-feed-xml-example.md) 
- [<span data-ttu-id="bdd02-117">Outlook Esquema XML del proveedor de Social Connector</span><span class="sxs-lookup"><span data-stu-id="bdd02-117">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)


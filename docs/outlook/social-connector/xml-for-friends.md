---
title: XML para amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: El elemento friends del esquema XML del proveedor de Microsoft Outlook Social Connector (OSC) permite a un proveedor de OSC especificar información para una lista de personas asociadas con un usuario de Outlook en la red social.
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361162"
---
# <a name="xml-for-friends"></a>XML para amigos

El elemento **friends** del esquema XML del proveedor de Microsoft Outlook Social Connector (OSC) permite a un proveedor de OSC especificar información para una lista de personas asociadas con un usuario de Outlook en la red social. Si el proveedor de OSC admite la sincronización en caché, esta lista de personas solo contendrá amigos del usuario Outlook en la red social. Si el OSC admite la sincronización híbrida o a petición, esta lista puede contener tanto amigos como no amigos del Outlook usuario. 

Cada persona de la lista se representa como un elemento **de** persona en el esquema XML, que admite detalles como el nombre, el apellido y las direcciones de correo electrónico. Los proveedores de OSC usan los **elementos de** amigos y personas independientemente de cómo quieran que el OSC sincronice la información de amigos desde la red social.  Tenga en cuenta  que los elementos secundarios de la persona son similares a algunas de las propiedades de un contacto de Outlook, lo que facilita el almacenamiento de amigos en una carpeta de contactos de Outlook específica de la red social, si la red social admite la sincronización híbrida o caché de amigos en una carpeta de contactos de Outlook. 

## <a name="example-scenarios"></a>Escenarios de ejemplo

En los escenarios de ejemplo siguientes se muestra la API de extensibilidad del proveedor de OSC que implementa un proveedor de OSC y la OSC realiza para obtener información de amigos. La información se expresa en cadenas XML que se ajustan al esquema XML del proveedor de OSC.
  
Para obtener un ejemplo de XML de amigos, vea [Friends XML Example](friends-xml-example.md). Para obtener más información acerca de la sincronización de la información de los amigos, vea [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Escenario 1: obtener una lista de amigos

Escenario 1: OSC obtiene una lista de amigos y un objeto [ISocialPerson](isocialpersoniunknown.md) y una imagen para cada amigo: 
    
1. Un proveedor de OSC que admite mostrar amigos del sitio de red social y permitir que el OSC almacenar en caché información de amigos indica que para el OSC mediante los elementos **getFriends** y **cacheFriends,** que son elementos secundarios del elemento **capabilities.** 
    
2. El proveedor de OSC también implementa los métodos [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)y [ISocialPerson::GetPicture.](isocialperson-getpicture.md) 
    
3. El OSC llama a **ISocialProvider::GetCapabilities** para comprobar el valor de los siguientes elementos: **getFriends** para comprobar que el proveedor de OSC admite mostrar amigos de la red social y **cacheFriends** para comprobar que el proveedor admite el almacenamiento en caché de amigos. 
    
4. El OSC llama **a ISocialSession::GetPerson** para obtener un objeto **ISocialPerson** para el Outlook usuario. 
    
5. El OSC llama a **ISocialPerson::GetFriendsAndColleagues** para obtener la lista de amigos del usuario Outlook devuelta en la cadena del parámetro _personCollection._ La  _cadena personCollection_ cumple con la definición de esquema XML del **elemento friends** en el esquema XML. 
    
6. Para cada amigo de la cadena XML  _personCollection,_ el OSC obtiene el valor del elemento **userID** para llamar a **ISocialSession::GetPerson** para obtener un objeto **ISocialPerson** para ese amigo. 
    
7. Para cada amigo de la cadena XML **personCollection,** el OSC llama a [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obtener un recurso de imagen para ese amigo. 
    
   El OSC puede realizar más llamadas en el objeto **ISocialPerson** para obtener actividades y detalles (por ejemplo, direcciones de correo electrónico) para ese amigo. 
    
### <a name="scenario-2-synchronize-friends"></a>Escenario 2: sincronizar amigos 

Escenario 2: OSC sincroniza a los amigos dinámicamente:
    
1. Un proveedor de OSC que admite la sincronización a petición de amigos y no amigos indica que para el OSC mediante los elementos **getFriends** y **dynamicContactsLookup.** El proveedor de OSC también establece el **elemento hashFunction.** Los tres elementos son elementos secundarios de las **capacidades**. 
    
2. El proveedor de OSC también implementa el [método ISocialSession2::GetPeopleDetails.](isocialsession2-getpeopledetails.md) 
    
3. El OSC llama a **ISocialProvider::GetCapabilities** para comprobar los valores de **getFriends** y **dynamicContactsLookup** para comprobar que el proveedor de OSC admite amigos y sincronización a petición de amigos y no amigos. El OSC también toma nota del valor de **hashFunction** admitido por el proveedor de OSC. 
    
4. Para cada usuario que se muestra en el Panel de personas, el OSC recopila la dirección de correo electrónico del usuario y la cifra mediante la función hash especificada en **hashFunction**. Esto forma una cadena XML que se ajusta a la definición de esquema XML para el **elemento hashedAddresses.** 
    
5. El OSC llama **a ISocialSession2::GetPeopleDetails**, proporcionando esta cadena XML de direcciones hash como el parámetro _personAddresses,_ para obtener dinámicamente detalles actualizados para las personas del parámetro _personsCollection._ La  _cadena de parámetro personsCollection_ cumple con la definición de esquema XML para el elemento **friends** del esquema XML. 

## <a name="parent-and-child-elements"></a>Elementos primarios y secundarios

Los siguientes son los dos elementos de nivel superior del **esquema de** amigos. 
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**amigos** <br/> |Representa el elemento raíz de una lista de **elementos person.** **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)y **ISocialSession2::GetPeopleDetails** devuelven cadenas XML que se ajustan a la definición de esquema del elemento **friends.**  <br/> |
|**person** <br/> |Representa una persona de una lista de **elementos de** persona. El [método ISocialPerson::GetDetails](isocialperson-getdetails.md) devuelve una cadena XML que se ajusta a la definición de esquema del **elemento person.**  <br/> |
   
En la tabla siguiente se describe cada elemento secundario del elemento **person** en el esquema XML del proveedor de OSC. 
  
Para obtener una definición completa del esquema XML del proveedor de OSC, incluidos los elementos necesarios u opcionales, vea Outlook Esquema XML del proveedor de [conectores sociales](outlook-social-connector-provider-xml-schema.md).
  
|**Elemento**|**Descripción**|
|:-----|:-----|
|**address** <br/> |Dirección física de la persona.  <br/> |
|**aniversario** <br/> |Fecha de aniversario de un evento para la persona.  <br/> |
|**askmeabout** <br/> |Temas de interés o experiencia de la persona.  <br/> |
|**birthday** <br/> |Fecha de nacimiento de la persona.  <br/> |
|**businessAddress** <br/> |Dirección física de la calle del lugar de trabajo de la persona.  <br/> |
|**businessCity** <br/> |Ciudad para el lugar de trabajo de la persona.  <br/> |
|**businessCountryOrRegion** <br/> |País o región del lugar de trabajo de la persona.  <br/> |
|**businessState** <br/> |Estado o provincia del lugar de trabajo de la persona.  <br/> |
|**businessZip** <br/> |Código postal o postal del lugar de trabajo de la persona.  <br/> |
|**celda** <br/> |Número de teléfono móvil de la persona.  <br/> |
|**city** <br/> |Ciudad de la dirección física de la persona.  <br/> |
|**company** <br/> |Nombre de la compañía asociada a la persona.  <br/> |
|**countryOrRegion** <br/> |País o región de la dirección física de la persona.  <br/> |
|**creationTime** <br/> |Hora de creación del perfil de la persona en la red social.  <br/> |
|**emailAddress** <br/> |Dirección de correo electrónico principal de la persona.  <br/> |
|**emailAddress2** <br/> |Dirección de correo electrónico secundaria de la persona.  <br/> |
|**emailAddress3** <br/> |Dirección de correo electrónico terciaria de la persona.  <br/> |
|**expirationTime** <br/> |Hora en que los datos de perfil de la persona expiran en la red social.  <br/> |
|**fileAs** <br/> |Cadena por la que la persona se va a presentar como contacto en un Outlook de contactos.  <br/> |
|**firstName** <br/> |Nombre o nombre de la persona.  <br/> |
|**friendStatus** <br/> |Estado de amigo de esta persona con el usuario que ha iniciado sesión en la red social. Debe ser uno de los siguientes valores: **friend**, **nonfriend**, **pending**, **pendingin**, **pendingout**.  <br/> |
|**fullName** <br/> |Nombre completo de la persona.  <br/> |
|**género** <br/> |Género de la persona. Debe ser uno de los siguientes valores: **varón**, **mujer**, **no especificado**.  <br/> |
|**homePhone** <br/> |Número de teléfono principal de la persona.  <br/> |
|**index** <br/> |Ubicación de la dirección hash de la persona en el parámetro de cadena _personsAddresses_ pasado a una llamada al método **ISocialSession2::GetPeopleDetails.** También indica el XML de **persona** de la persona en la cadena  _personsCollection_ devuelta por **GetPeopleDetails**.  <br/> |
|**industrias** <br/> |Industrias en las que la persona está involucrada.  <br/> |
|**interests** <br/> |Intereses o aficiones de la persona.  <br/> |
|**lastModificationTime** <br/> |Hora en que se modificó por última vez el perfil de la persona en la red social.  <br/> |
|**lastName** <br/> |Apellido o apellido de la persona.  <br/> |
|**location** <br/> |La ubicación de la persona.  <br/> |
|**alias** <br/> |Un nombre más corto o un nombre inventado de la persona.  <br/> |
|**otherAddress** <br/> |Dirección de calle alternativa de la persona.  <br/> |
|**otherCity** <br/> |Ciudad de la dirección alternativa de la persona.  <br/> |
|**otherCountryOrRegion** <br/> |País o región de la dirección alternativa de la persona.  <br/> |
|**otherState** <br/> |Estado o provincia de la dirección alternativa de la persona.  <br/> |
|**otherZip** <br/> |Código postal o postal de la dirección alternativa de la persona.  <br/> |
|**teléfono** <br/> |Número de teléfono de contacto principal de la persona.  <br/> |
|**pictureUrl** <br/> |Dirección URL de una imagen de perfil de la persona.  <br/> |
|**relación** <br/> |Relación de esta persona con el usuario que ha iniciado sesión.  <br/> |
|**schools** <br/> |Las escuelas a las que la persona va o a la que ha ido.  <br/> |
|**skills** <br/> |Habilidades personales de la persona.  <br/> |
|**state** <br/> |Estado o provincia de la dirección física de la persona.  <br/> |
|**title** <br/> |Designación agregada al nombre de la persona.  <br/> |
|**userID** <br/> |Id. para identificar a la persona en la red social.  <br/> |
|**webProfilePage** <br/> |Dirección de la página web que contiene un perfil de la persona.  <br/> |
|**sitio web** <br/> |Sitio web de la persona.  <br/> |
|**workPhone** <br/> |Número de teléfono de empresa de la persona.  <br/> |
|**zip** <br/> |Código postal o código postal de la dirección física de la persona.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Ejemplo de XML de amigos](friends-xml-example.md)  
- [Sincronizar amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML para funcionalidades](xml-for-capabilities.md) 
- [XML para actividades](xml-for-activities.md)
- [Desarrollo de un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)


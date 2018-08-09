---
title: XML para amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: El elemento de amigos en el esquema XML de proveedor de Microsoft Outlook Social Connector (OSC) permite que un proveedor de OSC especificar la información para obtener una lista de las personas asociadas con un usuario de Outlook en la red social.
ms.openlocfilehash: 07f1bb77e7912e3973fd2af8a70275642b72039c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821239"
---
# <a name="xml-for-friends"></a>XML para amigos

El elemento de **amigos** en el esquema XML de proveedor de Microsoft Outlook Social Connector (OSC) permite que un proveedor de OSC especificar la información para obtener una lista de las personas asociadas con un usuario de Outlook en la red social. Si el proveedor de OSC admite la sincronización de caché, esta lista de persona va a contener a sólo amigos del usuario de Outlook en la red social. Si el OSC admite la sincronización a petición o híbrida, esta lista puede contener amigos y que no sean de amigos del usuario de Outlook. 

Cada persona de la lista se representa como un elemento de la **persona** en el esquema XML, que es compatible con detalles como el nombre, apellidos y direcciones de correo electrónico. Proveedores de OSC utilizan los elementos de **amigos** y **persona** independientemente de cómo desean que el OSC para sincronizar la información de amigo desde la red social. Tenga en cuenta que los elementos secundarios de **persona** son similares a algunas de las propiedades de un contacto de Outlook, que facilita al almacenamiento amigos en una carpeta de contactos de Outlook específica a la red social, si la admite redes sociales en caché o híbrida sincronización de amigos a una carpeta de contactos de Outlook. 

## <a name="example-scenarios"></a>Escenarios de ejemplo

Los siguientes escenarios de ejemplo muestran al proveedor de OSC las llamadas de API de extensibilidad que implementa un proveedor de OSC y hace que el OSC para obtener información de amigo. Información se expresa en las cadenas XML que se ajustan al esquema XML de proveedor OSC.
  
Para obtener un ejemplo de amigos XML, vea [Ejemplo de XML de amigos](friends-xml-example.md). Para obtener más información acerca de cómo sincronizar información de amigos, consulte [sincronización de amigos y actividades](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Escenario 1: obtener una lista de amigos

Escenario 1: OSC Obtiene una lista de amigos y un objeto de [ISocialPerson](isocialpersoniunknown.md) y una imagen para cada uno de ellos: 
    
1. Un proveedor de OSC que admite que muestra a amigos desde el sitio de red social y lo que permite el OSC en caché la información de amigo que indica a la OSC mediante el uso de los elementos **getFriends** y **cacheFriends** , que son elementos secundarios de la ** capacidades de** elemento. 
    
2. El proveedor de OSC también implementa la [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)y métodos de [ISocialPerson::GetPicture](isocialperson-getpicture.md) . 
    
3. El OSC llama a **ISocialProvider::GetCapabilities** para comprobar el valor de los siguientes elementos: **getFriends** para comprobar que admite el proveedor OSC que muestra amigos desde las redes sociales y **cacheFriends** para comprobar que el proveedor admite el almacenamiento en caché de amigos. 
    
4. El OSC llama a **ISocialSession::GetPerson** para obtener un objeto **ISocialPerson** para el usuario de Outlook. 
    
5. El OSC llama a **ISocialPerson::GetFriendsAndColleagues** para obtener el usuario de Outlook de la lista de amigos devuelto en la cadena de parámetro _personCollection_ . La cadena _personCollection_ cumple con la definición del esquema XML para el elemento de **amigos** en el esquema XML. 
    
6. Para cada uno de ellos en la cadena XML _personCollection_ , el OSC Obtiene el valor del elemento **userID** para llamar a **ISocialSession::GetPerson** para obtener un objeto **ISocialPerson** para ese amigo. 
    
7. Para cada uno de ellos en la cadena XML **personCollection** , el OSC llama a [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obtener un recurso de imagen para ese amigo. 
    
   El OSC puede realizar más llamadas en el objeto **ISocialPerson** para obtener detalles (por ejemplo, direcciones de correo electrónico) y las actividades para ese amigo. 
    
### <a name="scenario-2-synchronize-friends"></a>Escenario 2: sincronizar amigos 

Escenario 2: OSC sincroniza amigos dinámicamente:
    
1. Un proveedor de OSC que admite la sincronización a petición de amigos y amigos que no sean indica el OSC mediante el uso de los elementos **getFriends** y **dynamicContactsLookup** . El proveedor de OSC también establece el elemento **hashFunction** . Los tres elementos son elementos secundarios de **las capacidades**. 
    
2. El proveedor de OSC también implementa el método [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md) . 
    
3. El OSC llama a **ISocialProvider::GetCapabilities** para comprobar si los valores de **getFriends** y **dynamicContactsLookup** para comprobar que es compatible con el proveedor de OSC amigos y sincronización a petición de amigos y amigos que no sean. El OSC también hace nota del valor de **hashFunction** admitidos por el proveedor OSC. 
    
4. Para cada usuario que se muestra en el panel de personas, el OSC recopila la dirección de correo electrónico del usuario y cifra mediante el uso de la función de hash especificada en **hashFunction**. Constituye una cadena XML que se ajusta a la definición del esquema XML para el elemento **hashedAddresses** . 
    
5. El OSC llama a **ISocialSession2::GetPeopleDetails**, proporcionar esta cadena XML de direcciones con algoritmo hash como el parámetro _personAddresses_ , para obtener detalles actualizados de forma dinámica para las personas en el parámetro _personsCollection_ . La cadena de parámetro _personsCollection_ cumple con la definición del esquema XML para el elemento de **amigos** en el esquema XML. 

## <a name="parent-and-child-elements"></a>Elementos primarios y secundarios

Los siguientes son los dos elementos de nivel superior en el esquema de **amigos** . 
  
|**Element**|**Descripción**|
|:-----|:-----|
|**amigos** <br/> |Representa el elemento raíz de una lista de elementos de la **persona** . El **ISocialPerson::GetFriendsAndColleagues**, [ISocialSession::FindPerson](isocialsession-findperson.md)y **ISocialSession2::GetPeopleDetails** devuelven cadenas XML que se ajustan a la definición de esquema del elemento **amigos** .  <br/> |
|**person** <br/> |Representa a una persona en una lista de elementos de la **persona** . El método [ISocialPerson::GetDetails](isocialperson-getdetails.md) devuelve una cadena XML que se ajusta a la definición de esquema del elemento de **persona** .  <br/> |
   
En la siguiente tabla se describe cada elemento secundario del elemento en el esquema XML de proveedor OSC **persona** . 
  
Para ver una definición completa del esquema XML de proveedor OSC, incluido qué elementos son obligatorios u opcionales, vea [Esquema de XML de Outlook Social Connector proveedor](outlook-social-connector-provider-xml-schema.md).
  
|**Element**|**Descripción**|
|:-----|:-----|
|**dirección** <br/> |Dirección física de la persona.  <br/> |
|**Aniversario** <br/> |Fecha de aniversario de un evento para la persona.  <br/> |
|**askmeabout** <br/> |Temas de interés o la experiencia de la persona.  <br/> |
|**cumpleaños** <br/> |Fecha de nacimiento de la persona.  <br/> |
|**businessAddress** <br/> |Dirección física del área de trabajo de la persona.  <br/> |
|**businessCity** <br/> |Ciudad de trabajo de la persona.  <br/> |
|**businessCountryOrRegion** <br/> |País o región del área de trabajo de la persona.  <br/> |
|**businessState** <br/> |Estado o provincia del área de trabajo de la persona.  <br/> |
|**businessZip** <br/> |ZIP o código postal del área de trabajo de la persona.  <br/> |
|**celda** <br/> |Número de teléfono móvil de la persona.  <br/> |
|**Ciudad** <br/> |Ciudad de la dirección física de la persona.  <br/> |
|**compañía** <br/> |Nombre de la compañía asociada con la persona.  <br/> |
|**countryOrRegion** <br/> |País o región de la dirección física de la persona.  <br/> |
|**creationTime** <br/> |Hora de creación del perfil de la persona en la red social.  <br/> |
|**emailAddress** <br/> |Dirección de correo electrónico principal de la persona.  <br/> |
|**emailAddress2** <br/> |Dirección de correo electrónico secundario de la persona.  <br/> |
|**emailAddress3** <br/> |Dirección de correo electrónico terciario de la persona.  <br/> |
|**expirationTime** <br/> |Hora en que expira datos del perfil de la persona en la red social.  <br/> |
|**Archivar como** <br/> |Cadena que es la persona que desea archivar como archivo de contactos de un contacto en Outlook.  <br/> |
|**firstName** <br/> |Nombre o nombre de la persona.  <br/> |
|**friendStatus** <br/> |Estado de confianza de esta persona con el usuario ha iniciado sesión en la red social. Debe ser uno de los siguientes valores: **friend**, **nonfriend**, **pendiente**, **pendingin**, **pendingout**.  <br/> |
|**fullName** <br/> |Nombre completo de la persona.  <br/> |
|**género** <br/> |Género de la persona. Debe ser uno de los siguientes valores: **masculino**, **femenino**, **no especificado**.  <br/> |
|**homePhone** <br/> |Número de teléfono del domicilio de la persona.  <br/> |
|**índice** <br/> |Ubicación de dirección con algoritmo hash de la persona en el parámetro de cadena de _personsAddresses_ que se pasa a una llamada al método **ISocialSession2::GetPeopleDetails** . También indica **persona** XML en la cadena de _personsCollection_ devuelta por **GetPeopleDetails la persona**.  <br/> |
|**sectores** <br/> |Sectores que la persona está ocupada en.  <br/> |
|**interests** <br/> |Intereses o aficiones de la persona.  <br/> |
|**lastModificationTime** <br/> |Hora en que se modificó por última vez el perfil de la persona en la red social.  <br/> |
|**lastName** <br/> |Último nombre o apellidos de la persona.  <br/> |
|**location** <br/> |La ubicación de la persona.  <br/> |
|**alias** <br/> |Un nombre más corto o un nombre arbitrario de la persona.  <br/> |
|**otherAddress** <br/> |Dirección postal alternativo de la persona.  <br/> |
|**otherCity** <br/> |Ciudad de dirección alternativa de la persona.  <br/> |
|**otherCountryOrRegion** <br/> |País o región de dirección alternativa de la persona.  <br/> |
|**otherState** <br/> |Estado o provincia de dirección alternativa de la persona.  <br/> |
|**otherZip** <br/> |ZIP o código postal de dirección alternativa de la persona.  <br/> |
|**teléfono** <br/> |Número de teléfono del contacto principal de la persona.  <br/> |
|**pictureUrl** <br/> |Dirección URL de una imagen de perfil de la persona.  <br/> |
|**Relación** <br/> |Relación de esta persona con el usuario ha iniciado la sesión.  <br/> |
|**escuelas** <br/> |Las escuelas que queda la persona o se ha producido un problema a.  <br/> |
|**skills** <br/> |Habilidades personales de la persona.  <br/> |
|**state** <br/> |Estado o provincia de la dirección física de la persona.  <br/> |
|**title** <br/> |Designación de agregado al nombre de la persona.  <br/> |
|**userID** <br/> |Identificador para identificar a la persona en la red social.  <br/> |
|**webProfilePage** <br/> |Dirección de página Web que contiene un perfil de la persona.  <br/> |
|**sitio Web** <br/> |Sitio web de la persona.  <br/> |
|**workPhone** <br/> |Número de teléfono de trabajo para la persona.  <br/> |
|**ZIP** <br/> |Código postal o código postal de la dirección física de la persona.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Ejemplo de XML de amigos](friends-xml-example.md)  
- [Sincronización de amigos y actividades](synchronizing-friends-and-activities.md)  
- [XML de capacidades](xml-for-capabilities.md) 
- [XML de actividades](xml-for-activities.md)
- [Desarrollar un proveedor con el esquema XML de OSC](developing-a-provider-with-the-osc-xml-schema.md)


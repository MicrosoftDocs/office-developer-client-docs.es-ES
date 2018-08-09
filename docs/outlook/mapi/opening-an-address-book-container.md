---
title: Abrir un contenedor de la libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 28f60154524065bd2c818e2e4b7db37ca33276b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818444"
---
# <a name="opening-an-address-book-container"></a>Abrir un contenedor de la libreta de direcciones

**Hace referencia a**: Outlook 
  
Después de abrir la MAPI integrado de la libreta de direcciones, abra uno o varios contenedores de libretas de direcciones para obtener acceso a los destinatarios dentro de ellos.
  
Para abrir el contenedor de nivel superior de la libreta de direcciones, llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) con un identificador de entrada NULL. 
  
Contenedores de la libreta de direcciones se pueden implementar con solo lectura o acceso de lectura y escritura. Contenedores de solo lectura se usan sólo para la exploración. Pueden modificarse contenedores de lectura y escritura, lo que permite a los clientes crear nuevas entradas y eliminar y modificar las entradas existentes. Todos los contenedores de (PAB) de la Libreta personal de direcciones se implementan como contenedores de lectura y escritura. 
  
Para abrir cualquier contenedor de nivel inferior, llamada **OpenEntry** y especifique el identificador de entrada del contenedor que se va a abrir. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Abra el contenedor designado como el archivo PAB
  
1. Llame a [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la Libreta personal de direcciones. 
    
2. Pase este identificador de entrada al [IAddrBook::OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Abra un contenedor que no es el archivo PAB
  
1. Llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) con un identificador de entrada NULL para abrir el contenedor de raíz de la libreta de direcciones. 
    
2. Llamar al método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para recuperar su tabla de jerarquía: una lista de todos los contenedores de nivel superior en la libreta de direcciones. 
    
3. Si el contenedor que se va a abrir es de un tipo específico:
    
   - Crear una estructura de **SPropertyRestriction** con **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para la etiqueta de propiedad, el tipo del contenedor para el valor de la propiedad y RELOP_EQ para la relación. **PR_DISPLAY_TYPE** se puede establecer en muchos valores, entre ellos: 
    
   - DT_GLOBAL para limitar la tabla de jerarquía para contenedores que pertenezcan a la lista global de direcciones.
    
   - DT_LOCAL para limitar la tabla a contenedores que pertenecen a una libreta de direcciones local.
    
   - DT_MODIFIABLE para limitar la tabla a los contenedores que se pueden modificar.
    
   - Crear una estructura de [elemento SPropTagArray](sproptagarray.md) que incluye la **entrada del objeto**, **PR_DISPLAY_TYPE**y cualquier otra columna de interés. 
    
   - Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de la etiqueta de propiedad. **HrQueryAllRows** devolverá cero o más filas, una fila por cada contenedor que pertenece al tipo especificado. Esté preparado para controlar la devolución de cualquier número de filas. 
    
   - Llame al método **IAddrBook::OpenEntry** con el identificador de entrada de la columna de **entrada del objeto** de la fila que representa el contenedor de interés. 
    
4. Si el contenedor que se va a abrir pertenece a un proveedor de libreta de direcciones específico:
    
   - Cree una estructura de [SPropertyRestriction](spropertyrestriction.md) con **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para la etiqueta de propiedad, un valor específico del proveedor para el valor de la propiedad y RELOP_EQ para la relación. Normalmente, el valor de específicas del proveedor es un identificador único global o GUID. Encontrará este valor publicado en uno de los archivos de encabezado del proveedor de libreta de direcciones. 
    
   - Crear una estructura de [elemento SPropTagArray](sproptagarray.md) que incluye la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**y cualquier otra columna de interés. 
    
   - Llame a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de la etiqueta de propiedad. **HrQueryAllRows** devolverá cero filas si el proveedor de libreta de direcciones especificado no está en el perfil. Puede devolver una o varias filas para contenedores de nivel superior del proveedor, dependiendo de cómo se organiza el proveedor. 
    
   - Llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) con el identificador de entrada de la columna de **entrada del objeto** de la fila que representa el contenedor de interés. Si el contenedor que le no interesa es un contenedor de nivel superior, busque el contenedor de nivel superior y atravesar la jerarquía. 
    


---
title: Abrir un contenedor de libreta de direcciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 89383b27-618c-4ccb-9e16-f66235c98bfe
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 97fa9f9750174c112c431c62f6171f674856fa86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436744"
---
# <a name="opening-an-address-book-container"></a>Abrir un contenedor de libreta de direcciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Después de abrir la libreta de direcciones MAPI integrada, abra uno o varios contenedores de la libreta de direcciones para tener acceso a los destinatarios que contiene.
  
Para abrir el contenedor de nivel superior de la libreta de direcciones, llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) con un identificador de entrada nulo. 
  
Los contenedores de la libreta de direcciones se pueden implementar con acceso de solo lectura o de lectura y escritura. Los contenedores de solo lectura solo se usan para examinar. Los contenedores de lectura y escritura se pueden modificar, lo que permite a los clientes crear nuevas entradas y eliminar y modificar las entradas existentes. Todos los contenedores de la libreta personal de direcciones (PAB) se implementan como contenedores de lectura y escritura. 
  
Para abrir cualquier contenedor de nivel inferior, llame a **OpenEntry** y especifique el identificador de entrada del contenedor que se va a abrir. 
  
## <a name="open-the-container-designated-as-the-pab"></a>Abrir el contenedor designado como PAB
  
1. Llame a [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar el identificador de entrada de la PAB. 
    
2. Pase este identificador de entrada a [IAddrBook:: OpenEntry](iaddrbook-openentry.md).
    
## <a name="open-a-container-that-is-not-the-pab"></a>Abrir un contenedor que no es la PAB
  
1. Llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) con un identificador de entrada null para abrir el contenedor raíz de la libreta de direcciones. 
    
2. Llame al método [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md) del contenedor raíz para recuperar su tabla de jerarquías, una lista de todos los contenedores de nivel superior de la libreta de direcciones. 
    
3. Si el contenedor que se va a abrir es de un tipo específico:
    
   - Cree una estructura **SPropertyRestriction** con **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para la etiqueta de propiedad, el tipo de contenedor para el valor de propiedad y RELOP_EQ para la relación. **PR_DISPLAY_TYPE** se puede establecer en muchos valores, entre ellos: 
    
   - DT_GLOBAL para limitar la tabla de jerarquía a los contenedores que pertenecen a la lista global de direcciones.
    
   - DT_LOCAL para limitar la tabla a contenedores que pertenecen a una libreta de direcciones local.
    
   - DT_MODIFIABLE para limitar la tabla a los contenedores que se pueden modificar.
    
   - Cree una estructura [SPropTagArray](sproptagarray.md) que incluya **** el **PR_DISPLAY_TYPE**, las demás columnas de interés. 
    
   - Llamar a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de etiquetas de propiedad. **HrQueryAllRows** devolverá cero o más filas, una fila por cada contenedor que pertenezca al tipo especificado. Prepárese para controlar la devolución de cualquier número de filas. 
    
   - Llame a **IAddrBook:: OpenEntry** con el identificador de entrada de **** la columna de elementos de la fila que representa el contenedor de interés. 
    
4. Si el contenedor que se va a abrir pertenece a un proveedor específico de la libreta de direcciones:
    
   - Cree una estructura [SPropertyRestriction](spropertyrestriction.md) con **PR_AB_PROVIDERS** ([PidTagAbProviders](pidtagabproviders-canonical-property.md)) para la etiqueta de propiedad, un valor específico del proveedor para el valor de la propiedad y RELOP_EQ para la relación. Normalmente, el valor específico del proveedor es un identificador único global o GUID. Este valor se publicará en uno de los archivos de encabezado del proveedor de la libreta de direcciones. 
    
   - Cree una estructura SPropTagArray que incluya **** el [](sproptagarray.md) ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_AB_PROVIDERS**y cualquier otra columna de interés. 
    
   - Llamar a [HrQueryAllRows](hrqueryallrows.md), pasando la restricción de propiedad y la matriz de etiquetas de propiedad. **HrQueryAllRows** devolverá cero filas si el proveedor de libreta de direcciones especificado no está en el perfil. Puede devolver una o más filas para los contenedores de nivel superior del proveedor, en función de cómo esté organizado el proveedor. 
    
   - Llame a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) con el identificador de entrada de **** la columna de elementos de la fila que representa el contenedor de interés. Si el contenedor que le interesa no es un contenedor de nivel superior, busque el contenedor de nivel superior y recorra la jerarquía. 
    


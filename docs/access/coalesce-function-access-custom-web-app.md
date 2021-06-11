---
title: Función Coalesce (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Devuelve la primera expresión que no es NULL de una lista de argumentos.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411396"
---
# <a name="coalesce-function-access-custom-web-app"></a>Función Coalesce (aplicación web personalizada de Access)

Devuelve la primera expresión que no es NULL de una lista de argumentos.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**Coalesce** (*Value*, [*Value*], ...,[*Value*]) 
  
La **función Coalesce** contiene los argumentos siguientes 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Valor*  <br/> |Expresión.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si todos los argumentos son NULL, **Coalesce** devuelve NULL. 
  
## <a name="example"></a>Ejemplo

La siguiente expresión se usa como regla de validación para una tabla. La expresión garantiza que las entradas se realizan en los campos Nombre, Apellido, Correo electrónico, Teléfono móvil, Trabajo Teléfono, Inicio Teléfono y Empresa antes de que se confirma un registro. Si alguno de los campos enumerados se deja en blanco, la función **Coalesce** devuelve Null, lo que infringe la regla de validación. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```



---
title: Combina los función (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Devuelve la primera expresión que no es nula de una lista de argumentos.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815332"
---
# <a name="coalesce-function-access-custom-web-app"></a>Combina los función (aplicación web personalizado de Access)

Devuelve la primera expresión que no es nula de una lista de argumentos.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

**Combina los** (*Valor*, [*valor*],..., [*valor*]) 
  
La función de **combinación** contiene los siguientes argumentos 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Value*  <br/> |Una expresión.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si todos los argumentos son NULL, **Coalesce** devuelve NULL. 
  
## <a name="example"></a>Ejemplo

La siguiente expresión se usa como la regla de validación para una tabla. La expresión se asegura de que las entradas se realizan en los campos nombre de la primera, última nombre, correo electrónico, teléfono móvil, trabajo teléfono, principal, y compañía telefónica antes de confirmar un registro. Si cualquiera de los campos enumerados se deja en blanco, la función de **combinación** devuelve Null, lo que infringe la regla de validación. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```



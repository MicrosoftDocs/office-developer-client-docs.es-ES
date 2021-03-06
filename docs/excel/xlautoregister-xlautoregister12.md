---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- función xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421168"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel llama a la función [xlAutoRegister](xlautoregister-xlautoregister12.md) siempre que se haya realizado una llamada a la función **XLM REGISTER** o a la función [xlfRegister](xlfregister-form-1.md)equivalente de la API de C, faltando los tipos de argumento y de devolución de la función. Permite al XLL buscar en sus listas internas de funciones exportadas y comandos para registrar la función con el argumento y los tipos devueltos especificados.
  
A partir de Excel 2007, Excel llama a la función **xlAutoRegister12** con preferencia a la función **xlAutoRegister** si la exporta XLL. 
  
Excel requiere un XLL para implementar y exportar ninguna de estas funciones.
  
> [!NOTE]
> Si **xlAutoRegister** /  **xlAutoRegister12** intenta registrar la función sin proporcionar el argumento y los tipos devueltos, se produce un bucle de llamada recursiva que, finalmente, desborda la pila de llamadas y se bloquea Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parameters

 _pxName_ (**xltypeStr**)
  
Nombre de la función XLL que se está registrando.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La función debe devolver el resultado del intento de registrar la función XLL _pxName_ mediante la **función xlfRegister.** Si la función especificada no es una de las exportaciones de XLL, debe devolver el **#VALUE!** error, o **NULL** que Excel interpretará en **#VALUE!**.
  
## <a name="remarks"></a>Comentarios

La implementación de **xlAutoRegister** debe realizar una búsqueda entre mayúsculas y minúsculas a través de las listas internas de funciones y comandos de XLL que exporta en busca de una coincidencia con el nombre pasado. Si se encuentra la función o el comando, **xlAutoRegister** debe intentar registrarla, mediante la función **xlfRegister,** asegurándose de proporcionar la cadena que indica a Excel los tipos de argumento y de devolución de la función, así como cualquier otra información necesaria acerca de la función. A continuación, debe volver a Excel sea cual sea la llamada a **xlfRegister devuelta.** Si la función se registró correctamente, **xlfRegister** devuelve un **valor xltypeNum** que contiene el id. de registro de la función. 
  
### <a name="example"></a>Ejemplo

Vea el archivo  `SAMPLES\EXAMPLE\EXAMPLE.C` para obtener un ejemplo de implementación de esta función. 
  
## <a name="see-also"></a>Vea también



[REGISTER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)


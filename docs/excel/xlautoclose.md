---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- función xlAutoClose [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815731"
---
# <a name="xlautoclose"></a>xlAutoClose

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel la llama cuando se desactiva el XLL. El complemento se desactiva cuando finaliza una sesión de Excel normal. El usuario puede desactivar el complemento durante una sesión de Excel y en ese caso se llamará a esta función.
  
Excel no requiere un XLL para implementar y exportar esta función, aunque es aconsejable para que el XLL pueda anular el registro de los comandos y funciones, liberar recursos, deshacer las personalizaciones y así sucesivamente. Si el XLL no anula explícitamente el registro de los comandos y funciones, Excel realiza este proceso después de llamar a la función **xlAutoClose**. 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>Parámetros

Esta función no toma ningún argumento.
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

La implementación de esta función debe devolver 1 (**int**).
  
## <a name="remarks"></a>Comentarios

Excel llama a la función **xlAutoClose** cuando se desactiva el XLL, es decir, se descarga de la memoria. El XLL se desactiva en las siguientes situaciones: 
  
- Al final normal de una sesión de Excel si está activo durante la sesión.
    
- Si se descargó explícitamente durante una sesión de Excel.
    
- Un XLL puede descargarse de varias formas:
    
- Usando el Administrador de complementos.
    
- Desde otro XLL que llama a [xlfUnregister](xlfunregister-form-1.md) con el nombre de este archivo DLL como argumento único. 
    
- Desde una hoja de macro de XLM que llama a [UNREGISTER](xlfunregister-form-1.md) con el nombre de este archivo DLL como argumento único. 
    
Esta función debe hacer lo siguiente:
  
- Quitar los menús o elementos de menú que ha agregado el XLL.
    
- Realizar cualquier limpieza global necesaria.
    
- Eliminar los nombres que se crearon, especialmente los nombres de las funciones exportadas. Recuerde que registrar funciones puede provocar que se creen algunos nombres, si el cuarto argumento para **REGISTER** está presente. 
    
## <a name="example"></a>Ejemplo

Ver los archivos `SAMPLES\EXAMPLE\EXAMPLE.C` y `SAMPLES\GENERIC\GENERIC.C` para las implementaciones de ejemplo de esta función. El código siguiente es de `SAMPLES\GENERIC\GENERIC.C`.
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>Vea también



[xlAutoOpen](xlautoopen.md)


[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)


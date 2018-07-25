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
# <a name="xlautoclose"></a><span data-ttu-id="ff9bb-104">xlAutoClose</span><span class="sxs-lookup"><span data-stu-id="ff9bb-104">xlAutoClose</span></span>

 <span data-ttu-id="ff9bb-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ff9bb-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ff9bb-106">Microsoft Excel la llama cuando se desactiva el XLL.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-106">Called by Microsoft Excel whenever the XLL is deactivated.</span></span> <span data-ttu-id="ff9bb-107">El complemento se desactiva cuando finaliza una sesión de Excel normal.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-107">The add-in is deactivated when an Excel session ends normally.</span></span> <span data-ttu-id="ff9bb-108">El usuario puede desactivar el complemento durante una sesión de Excel y en ese caso se llamará a esta función.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-108">The add-in can be deactivated by the user during an Excel session, and this function will be called in that case.</span></span>
  
<span data-ttu-id="ff9bb-109">Excel no requiere un XLL para implementar y exportar esta función, aunque es aconsejable para que el XLL pueda anular el registro de los comandos y funciones, liberar recursos, deshacer las personalizaciones y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-109">Excel does not require an XLL to implement and export this function, although it is advisable so that your XLL can unregister functions and commands, release resources, undo customizations, and so on.</span></span> <span data-ttu-id="ff9bb-110">Si el XLL no anula explícitamente el registro de los comandos y funciones, Excel realiza este proceso después de llamar a la función **xlAutoClose**.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-110">If functions and commands are not explicitly unregistered by the XLL, Excel does this after calling the **xlAutoClose** function.</span></span> 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a><span data-ttu-id="ff9bb-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff9bb-111">Parameters</span></span>

<span data-ttu-id="ff9bb-112">Esta función no toma ningún argumento.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-112">This function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="ff9bb-113">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff9bb-113">Property value/Return value</span></span>

<span data-ttu-id="ff9bb-114">La implementación de esta función debe devolver 1 (**int**).</span><span class="sxs-lookup"><span data-stu-id="ff9bb-114">Your implementation of this function must return 1 (**int**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff9bb-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ff9bb-115">Remarks</span></span>

<span data-ttu-id="ff9bb-116">Excel llama a la función **xlAutoClose** cuando se desactiva el XLL, es decir, se descarga de la memoria.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-116">Excel calls the **xlAutoClose** function whenever the XLL is deactivated, that is, unloaded from memory.</span></span> <span data-ttu-id="ff9bb-117">El XLL se desactiva en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="ff9bb-117">The XLL is deactivated in the following situations:</span></span> 
  
- <span data-ttu-id="ff9bb-118">Al final normal de una sesión de Excel si está activo durante la sesión.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-118">At the normal end of an Excel session if active during that session.</span></span>
    
- <span data-ttu-id="ff9bb-119">Si se descargó explícitamente durante una sesión de Excel.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-119">If explicitly unloaded during an Excel session.</span></span>
    
- <span data-ttu-id="ff9bb-120">Un XLL puede descargarse de varias formas:</span><span class="sxs-lookup"><span data-stu-id="ff9bb-120">An XLOPER/XLOPER12 can be created in several ways:</span></span>
    
- <span data-ttu-id="ff9bb-121">Usando el Administrador de complementos.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-121">Using the Add-In Manager</span></span>
    
- <span data-ttu-id="ff9bb-122">Desde otro XLL que llama a [xlfUnregister](xlfunregister-form-1.md) con el nombre de este archivo DLL como argumento único.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-122">From another XLL that calls [xlfUnregister](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
- <span data-ttu-id="ff9bb-123">Desde una hoja de macro de XLM que llama a [UNREGISTER](xlfunregister-form-1.md) con el nombre de este archivo DLL como argumento único.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-123">From an XLM macro sheet that calls [UNREGISTER](xlfunregister-form-1.md) with the name of this DLL as the only argument.</span></span> 
    
<span data-ttu-id="ff9bb-124">Esta función debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ff9bb-124">This function should do the following:</span></span>
  
- <span data-ttu-id="ff9bb-125">Quitar los menús o elementos de menú que ha agregado el XLL.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-125">Remove any menus or menu items that were added by the XLL.</span></span>
    
- <span data-ttu-id="ff9bb-126">Realizar cualquier limpieza global necesaria.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-126">Perform any necessary global cleanup.</span></span>
    
- <span data-ttu-id="ff9bb-127">Eliminar los nombres que se crearon, especialmente los nombres de las funciones exportadas.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-127">Delete any names that were created, especially names of exported functions.</span></span> <span data-ttu-id="ff9bb-128">Recuerde que registrar funciones puede provocar que se creen algunos nombres, si el cuarto argumento para **REGISTER** está presente.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-128">Remember that registering functions may cause some names to be created, if the fourth argument to **REGISTER** is present.</span></span> 
    
## <a name="example"></a><span data-ttu-id="ff9bb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff9bb-129">Example</span></span>

<span data-ttu-id="ff9bb-130">Ver los archivos `SAMPLES\EXAMPLE\EXAMPLE.C` y `SAMPLES\GENERIC\GENERIC.C` para las implementaciones de ejemplo de esta función.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-130">See the files  `SAMPLES\EXAMPLE\EXAMPLE.C` and  `SAMPLES\GENERIC\GENERIC.C` for example implementations of this function.</span></span> <span data-ttu-id="ff9bb-131">El código siguiente es de `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="ff9bb-131">The following code is from  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="ff9bb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff9bb-132">See also</span></span>



[<span data-ttu-id="ff9bb-133">xlAutoOpen</span><span class="sxs-lookup"><span data-stu-id="ff9bb-133">xlAutoOpen</span></span>](xlautoopen.md)


[<span data-ttu-id="ff9bb-134">Administrador de complementos y funciones de la interfaz de XLL</span><span class="sxs-lookup"><span data-stu-id="ff9bb-134">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)


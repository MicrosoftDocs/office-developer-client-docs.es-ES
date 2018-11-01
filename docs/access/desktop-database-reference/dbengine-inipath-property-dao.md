---
title: DBEngine.IniPath Property (DAO)
TOCTitle: IniPath Property
ms:assetid: b18cace5-4e53-d011-6373-f4ac64556fd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822009(v=office.15)
ms:contentKeyID: 48547151
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053070
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 344f5b0a1edac379386208a831d332e8926654ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882962"
---
# <a name="dbengineinipath-property-dao"></a><span data-ttu-id="9ab38-102">DBEngine.IniPath Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9ab38-102">DBEngine.IniPath Property (DAO)</span></span>


<span data-ttu-id="9ab38-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ab38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9ab38-104">Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="9ab38-104">Sets or returns information about the Windows Registry key that contains values for the Microsoft Access database engine (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ab38-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ab38-105">Syntax</span></span>

<span data-ttu-id="9ab38-106">*expresión* . IniPath</span><span class="sxs-lookup"><span data-stu-id="9ab38-106">*expression* .IniPath</span></span>

<span data-ttu-id="9ab38-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="9ab38-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab38-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9ab38-108">Remarks</span></span>

<span data-ttu-id="9ab38-p101">Puede configurar el motor de base de datos Microsoft Access con el Registro de Windows. Puede utilizar el Registro para configurar opciones, tales como los archivos DLL de un archivo ISAM instalable.</span><span class="sxs-lookup"><span data-stu-id="9ab38-p101">You can configure the Microsoft Access databse engine with the Windows Registry. You can use the Registry to set options, such as installable ISAM DLLs.</span></span>

<span data-ttu-id="9ab38-p102">Para que esta opción funcione, debe establecer la propiedad **IniPath** antes de que su aplicación llame a cualquier otro código DAO. El ámbito de esta configuración está limitado a la aplicación y no se puede cambiar sin reiniciar ésta.</span><span class="sxs-lookup"><span data-stu-id="9ab38-p102">For this option to have any effect, you must set the **IniPath** property before your application invokes any other DAO code. The scope of this setting is limited to your application and can't be changed without restarting your application.</span></span>

<span data-ttu-id="9ab38-p103">Utilice también el Registro para proporcionar parámetros de inicialización para algunos controladores de base de datos ISAM instalables. Por ejemplo, para utilizar la versión 4.0 de Paradox, establezca la propiedad **IniPath** como parte del Registro con los parámetros apropiados.</span><span class="sxs-lookup"><span data-stu-id="9ab38-p103">You also use the Registry to provide initialization parameters for some installable ISAM database drivers. For example, to use Paradox version 4.0, set the **IniPath** property to a part of the Registry containing the appropriate parameters.</span></span>

<span data-ttu-id="9ab38-115">Esta propiedad reconoce alguno HKEY\_LOCAL\_máquina o HKEY\_LOCAL\_usuario.</span><span class="sxs-lookup"><span data-stu-id="9ab38-115">This property recognizes either HKEY\_LOCAL\_MACHINE or HKEY\_LOCAL\_USER.</span></span> <span data-ttu-id="9ab38-116">Si no hay ninguna clave de raíz se proporciona, el valor predeterminado es HKEY\_LOCAL\_máquina.</span><span class="sxs-lookup"><span data-stu-id="9ab38-116">If no root key is supplied, the default is HKEY\_LOCAL\_MACHINE.</span></span>


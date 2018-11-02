---
title: Handler (propiedad, RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bb9444091611fbd051da9fa649b5d3efdb92ee6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923584"
---
# <a name="handler-property-rds"></a><span data-ttu-id="ee2d6-102">Handler (propiedad, RDS)</span><span class="sxs-lookup"><span data-stu-id="ee2d6-102">Handler property (RDS)</span></span>


<span data-ttu-id="ee2d6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee2d6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ee2d6-104">Indica el nombre de un programa de personalización del servidor (controlador) que amplía la funcionalidad de [RDSServer.DataFactory](datafactory-object-rdsserver.md) y de cualquier parámetro utilizado por el *controlador*.</span><span class="sxs-lookup"><span data-stu-id="ee2d6-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee2d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee2d6-105">Syntax</span></span>

<span data-ttu-id="ee2d6-106">*DataControl*. Controlador = *cadena*</span><span class="sxs-lookup"><span data-stu-id="ee2d6-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="ee2d6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee2d6-107">Parameters</span></span>

  - <span data-ttu-id="ee2d6-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="ee2d6-108">*DataControl*</span></span>

  - <span data-ttu-id="ee2d6-109">Variable de objeto que representa un objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ee2d6-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="ee2d6-110">*String*</span><span class="sxs-lookup"><span data-stu-id="ee2d6-110">*String*</span></span>

  - <span data-ttu-id="ee2d6-111">Un valor de **tipo String** que contiene el nombre del controlador y de cualquier parámetro, todo separado por comas (por ejemplo, "handlerName, parm1, parm2,..., parm *N"*).</span><span class="sxs-lookup"><span data-stu-id="ee2d6-111">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee2d6-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee2d6-112">Remarks</span></span>

<span data-ttu-id="ee2d6-113">Esta propiedad admite personalización, una funcionalidad que exige el establecimiento de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="ee2d6-113">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="ee2d6-p101">El nombre del controlador y sus parámetros, si los hubiera, se separan mediante comas (","). La aparición de un punto y coma (";") en algún lugar de *String* dará lugar a un comportamiento impredecible. Puede escribir su propio controlador siempre que admita la interfaz **IDataFactoryHandler**.</span><span class="sxs-lookup"><span data-stu-id="ee2d6-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="ee2d6-p102">El nombre del controlador predeterminado es **MSDFMAP.Handler**, mientras que su parámetro predeterminado es un archivo de personalización denominado **MSDFMAP.INI**. Utilice esta propiedad para llamar a archivos de personalización alternativos creados por el administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="ee2d6-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="ee2d6-119">La alternativa a establecer la propiedad **Handler** es especificar un controlador y parámetros en la propiedad [ConnectionString](connectionstring-property-ado.md) ; es decir, "\**controlador = \*\*\* handlerName, parm1, parm2,...;*".</span><span class="sxs-lookup"><span data-stu-id="ee2d6-119">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>


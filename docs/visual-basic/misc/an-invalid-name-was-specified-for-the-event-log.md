---
title: 为事件日志指定了无效名称
ms.date: 07/20/2015
ms.assetid: b1b158bd-f13f-4371-a8af-31c0e86ae6be
ms.openlocfilehash: 8b6df077f15744cd2c34fb9e7e148b02ea27d5bf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33598058"
---
# <a name="an-invalid-name-was-specified-for-the-event-log"></a>为事件日志指定了无效名称
为事件日志指定了无效名称。 通常名称中存在无效字符、文件名太长或空白文件名会导致此结果。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
-   如果指定的名称多于 8 个字符，请确保与其他事件日志名称之间不存在冲突。 当确定名称是否唯一时，将仅计算前八个字符。  
  
-   如果提供路径，请确保它被正确解析。  
  
-   检查此名称中是否不存在任何无效字符。 不能在文件名中使用的字符包括 `<`、 `>`、 `:`、 `"`、 `/`、 `\`和 `|`。  
  
## <a name="see-also"></a>请参阅  
 [如何：分析文件路径](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-parse-file-paths.md)  
 [如何：重命名文件](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-rename-a-file.md)  
 
